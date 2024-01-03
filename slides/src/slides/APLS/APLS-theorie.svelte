<section id="APLS-theorie">
    
    <section id="APLS-title" data-background-image="img/think-math.gif" data-background-opacity="0.2">

        <h1>Alternative-PLS</h1>

        <p>la réponse à un problème de développement théorique</p>

    </section>

    <section id="APLS-theorie-overview" style="font-size: 0.6em;">

        <h2>overview</h2>

        {`$$
        \\begin{array}{rccll}

        & & c(s,t) = \\sum c_i \\overset{\\textsf{base ACP } \\left(✅ \\underset{\\Vert \\cdot \\Vert}{\\perp} \\right)}{\\boxed{\\phi_i(s) \\phi_i(t)}}
        \\\\

        & & \\downarrow

        \\\\

        & \\rightarrow&

        \\underset{\\textsf{développement } \\operatorname{vect}\\left(c^k[b]\\right)_{1,p}}{
        \\boxed{

        \\tilde{m}_p^{[c]}
        }
        }

        & \\leftarrow & \\textsf{pour dvp la théorie}
        & \\left[
        \\begin{array}{c}
        \\textsf{base non } {\\perp}
        \\\\
        \\textsf{explicite}
        \\end{array}
        \\right]

        \\\\

        m(x) & & \\Updownarrow &

        \\\\

        &\\rightarrow&

        \\underset{\\textsf{base PLS }}
        {
        \\boxed{

        \\tilde{m}_p^{[\\psi]}

        }
        }

        & \\leftarrow & \\textsf{pour la pratique}
        & \\left[
        \\begin{array}{c}
        \\textsf{base } \\underset{\\Vert \\cdot \\Vert}{\\perp}
        \\\\
        \\textsf{non explicite}
        \\end{array}
        \\right]

        \\\\

        \\end{array}
        $$`}

        <p class="fragment fade-down">
            puis on va mettre des chapeaux car on est statisticiens 🤓
        </p>

        <p class="fragment fade-down">
            et on va pleurer à regarder {`$\\Vert \\hat m_p - m \\Vert$`} car on est matheux ☠️
        </p>

    </section>

    <section id="APLS-theorie-psi-dans-C" style="font-size: 0.7em;">

        <h1>① équivalence ①</h1>

        <p class="fragment fade-in-then-semi-out"> on aimerait montrer que {`$\\forall p \\quad \\psi_p = \\sum a_i c^i[b]$`}

            <br>

            ie : {`$\\psi_p \\in \\operatorname{vect} \\left( c^i[b] \\right)_{1,p}$`}
        </p>

        <p class="fragment fade-down">{`$\\psi_p \\in \\frac{ \\operatorname{vect} \\left( c^i[b] \\right)_{1,p} }{\\operatorname{sign}} = \\mathcal C_{1,p}[b]$`}</p>

        <br>

        <p class="fragment fade-in-then-out">{`$P_{F_p(\\psi)}^\\perp \\left[ f \\in \\mathcal C^0(K, \\mathbb R) \\right] \\in \\operatorname{vect}(\\psi_i)_{1,p} \\subset \\mathcal C_{1,p}[f]$`}</p>

        <p class="fragment fade-in-then-out">{`$P_{F_p(\\psi)}^\\perp \\left[ f \\in \\mathcal C^0(K, \\mathbb R) \\right] \\in \\operatorname{vect}(\\psi_i)_{1,p} = \\mathcal C_{1,p}[f]$`}</p>

    </section>

    <section id="PLS-determination-de-la-base" style="font-size: 0.7em;">

        <h3>construction de la base PLS {`$\\; \\psi$`}</h3>

        <strong>théorème [3.1]</strong>

        {`$$
        \\boxed{
        \\int _K \\mathbb E[X^2](u)du < \\infty
        }
        \\implies
        \\boxed{
        \\begin{array}{l}
        \\exists ! \\gamma \\in \\mathbb R^p \\\\
        \\rightarrow  \\psi_p = \\gamma_0 \\left( c \\left[ \\, b - P_{F_{p-1}(\\psi)}(b) \\right] + \\sum_{k=1}^{p-1} \\gamma_k \\psi_k \\,  \\right)
        \\\\
        \\rightarrow \\langle \\psi_k \\vert \\psi_p \\rangle_{c(\\cdot, \\cdot)} = 0 \\quad k < p
        \\\\
        \\rightarrow \\Vert \\psi_p \\Vert = 1
        \\end{array}
        }
        $$`}

        <p>
            on a :
            {`$\\psi_p = \\Gamma_p( c[\\cdot], b , \\psi_{1:p-1} )\\quad$ et donc $\\quad \\psi_p = \\sum\\limits_{i=1}^p u_i c^i[b]$`}
        </p>
        <p>
            {`$\\implies \\operatorname{dim} < \\infty \\quad \\tilde m_p^{[\\psi]} \\iff  \\tilde m_p^{[c]}$`}
        </p>

    </section>

    <section>

        <p class="fragment semi-fade-out">
            {`$\\psi_1 = \\frac{c[b]}{\\Vert c[b] \\Vert}$`} (3.1)
        </p>

        <p class="fragment fade-in-then-semi-out">
            {`$\\psi_2 = \\alpha_0( c[b - \\langle b \\vert \\psi_1 \\rangle \\psi_1] + \\alpha_1 \\frac{c[b]}{\\Vert c[b] \\Vert} )$`} (3.1)
        </p>

        <p class="fragment fade-in-then-semi-out">
            {`$c[ c[b] ] = c^2[b]$`} (base ACP : mercer)
        </p>

        <p class="fragment fade-in-then-semi-out">{`$\\implies \\psi_p = \\sum_i^p a_i c^i[b]$`}</p>

        <p class="fragment fade-in"> ⚠️ ne pas oublier que c'est au signe près car :

            <br>

            {`$\\alpha_0$ déterminé par $\\Vert \\psi_p \\Vert = 1$`}
        </p>

    </section>

    <section id="APLS-theorie-estimation-de-b" style="font-size: 0.7em;">

        <p>maintenant on aimerait bien les estimer, {`$k = \\begin{bmatrix} \\vdots \\\\ k_i \\\\ \\vdots \\end{bmatrix}_{1,p}$`} qui vérifient </p>

        <p>

            {`$$
            \\begin{align}
            m(x) &= \\mathbb E[Y] + \\langle \\, X - \\mu \\, \\vert \\, b \\, \\rangle
            \\\\
            \\tilde m_p^{[c]}(x) &= \\mathbb E[Y] + \\langle \\, X - \\mu \\, \\vert \\, \\sum\\limits_{i=1}^p k_i c^i [b] \\, \\rangle

            \\end{align}
            $$`}
        </p>

        <p class="fragment fade-down">

            {`$$\\left( k_i \\right)_{1,p} = \\underset{
            (a_i)_{1,p}}
            {\\operatorname{argmin}}
            \\mathbb E \\left[
            \\left(
            \\underbrace{
            \\langle \\, X - \\mu \\, \\vert \\, b \\, \\rangle - \\langle \\, X - \\mu \\, \\vert \\, \\sum\\limits_{i=1}^p a_i c^i [b] \\, \\rangle
            }_{
            m(X) - \\tilde m_p^{[c] } (X)
            }
            \\right)^2
            \\right]$$`}
        </p>

    </section>

    <section id="APLS-theorie-convergence-de-bp" style="font-size: 0.7em;">

        <h1>② convergence ②</h1>
        <strong>théorème [3.2]</strong>

        <br>

        <p>{`$$\\begin{array}{c} \\mathbb E \\Vert X \\Vert^2 < \\infty \\\\ \\operatorname{sp} c[ \\, \\cdot \\, ] \\subset \\mathbb R_+^* \\end{array} \\implies b_p \\xrightarrow[p \\rightarrow \\infty]{\\mathbb L^2(K)} b$$`}</p>

        <p>et donc {`$\\boxed{b = \\sum\\limits_i^\\infty k_i c^i[b]}$`}</p>

        <p class="fragment fade-down">⚠️ pareil ne pas oublier que les $k_i$ ne sont pas uniques ⚠️</p>

    </section>

    <section id="APLS-theorie-lien-ACP" style="font-size: 0.7em;">

        <h2>expression de l'APLS dans la base ACP</h2>

        <br>

        <p>
            {`$$\\tilde b_p = \\sum_i^p k_i c^i[b] = \\sum_k^\\infty \\beta_k \\left( \\sum_i^p k_i c_k^i \\right) \\phi_k$$`}

        </p>

        <br>
        <br>
        rappel : {`$c(s,t) = \\sum_i c_i \\phi_i(s) \\phi_i(t)$`}

    </section>

</section>