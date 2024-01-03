<section id="Contexte">

    <section id="contexte-title" data-background-video="img/obama-confused.mp4" data-background-video-loop data-background-video-muted data-background-opacity="0.6">

        <h1>un peu de contexte</h1>
    </section>

    <section id="contexte-model">
        <h2>modèle</h2>

        {`$Y = a + \\displaystyle\\int_K b(u)X(u)du + \\varepsilon$`}

        <br />
        <br />

        <small>dans le cas de cet exposé (et du papier) : </small>

        <br />

        <span style="font-size: 0.6em;">
            {`
            $$\\begin{array}{rrcll}
            K & & & \\textsf{compact de } \\mathbb R & \\equiv \\textsf{intervalle fermé}
            \\\\
            a& &\\in& \\mathbb R & \\equiv scalaire
            \\\\
            b& : K \\rightarrow \\mathbb R &\\in& \\mathbb L^2(K) & \\equiv fcn
            \\\\
            \\varepsilon  & & \\in & m(\\Omega , \\mathbb R ) & \\equiv \\operatorname{VA}( \\mathbb R )
            \\\\
            X & & \\in & m\\left[ \\Omega, \\mathcal C^0( \\mathbb R, \\mathbb R ) \\right] & \\equiv \\operatorname{VA}\\left[ C^0( \\mathbb R, \\mathbb R ) \\right]
            \\\\
            Y && \\in & m(\\Omega , \\mathbb R) & \\equiv \\operatorname{VA}( \\mathbb R )
            \\end{array}$$
            `}
        </span>
    </section>

    <section>

        comment estimer {`$m(x) = \\mathbb E[ Y | X = x ] ?$`}

    </section>

    <section id="contexte-model-question">

        <i class="fa fa-question"></i> Comment trouver {`$a \\in \\mathbb R$`} et {`$b \\in \\mathbb L^2$`} <i class="fa fa-question"></i>

        <br /><br />

        <span class="fragment fade-down"> <i class="fa fa-warning"></i> {`$\\mathbb L^2$`} est de dimension {`$\\infty$`} <i class="fa fa-warning"></i>  </span>

        <span class="fragment fade-down"> {`$\\displaystyle\\sum_1^\\infty \\beta_i \\psi_i = b \\approx \\sum_{1}^p \\beta_i \\psi_i$`} </span>

    </section>

    <section id="contexte-b-et-sa-projection">
        <h3> <i class="fa fa-pencil"></i> Notations <i class="fa fa-pencil"></i></h3>

        <div class="flex-container" style="display: flex;">

            <div style="flex: 1; margin-right: 10px; border: 1.5px solid black;" class="fragment fade-in">
                <span style="font-size: 0.6em;">
                    base {`$( \\psi_i : K \\rightarrow \\mathbb R )$ de $\\mathbb L^2( K )$`}
                    {`$$F_n(\\psi) = \\operatorname{vect}( \\psi_i )_{1,n}$$`}
                    {`$$F_\\infty(\\psi) = \\operatorname{vect}( \\psi_i )_{\\mathbb N}=\\mathbb L^2(K)$$`}
                </span>
            </div>
            <div style="flex: 1;margin-left: 10px; border: 1.5px solid black;" class="fragment fade-in">
                <span style="font-size: 0.6em;">
                    {`$$b = \\sum\\limits_{\\mathbb N} \\underbrace{\\langle b \\vert \\psi_i \\rangle}_{\\beta_i} \\, \\psi_i$$`}

                    {`$$\\hat b_p^{[\\psi]} = P^\\perp_{F_p(\\psi)}( \\, b \\, ) = \\sum_{i=1}^p \\beta_i \\psi_i$$`}
                </span>
            </div>
        </div>

        <br />

        <p class="fragment fade-down">

            <i class="fa fa-question"></i> quelle base choisir <i class="fa fa-question"></i>
        </p>

    </section>

    <section>
        <!-- <i class="fa fa-mouse-pointer"></i>

<i class="fa fa-sticky-note"></i>
        <i class="fa fa-wikipedia-w"></i> -->
        <p><i class="fa fa-lightbulb-o"></i> projeter sur une base adaptée aux données <i class="fa fa-lightbulb-o"></i></p>

        <p class="fragment fade-down">nous appellerons cette base {`$\\phi = (\\phi_i)_{i \\in \\mathbb N}$`}</p>

    </section>

    <!-- —————————————————————————————————————— ACP Théorème de Mercer et rpz KL ——————————————————————————————————————————————— -->

    <section id="contexte-ACP-1">
        <h3> <i class="fa fa-flag"></i> ACP Fonctionnelle <i class="fa fa-flag"></i></h3>
        <span style="font-size: 0.7em;">[Partie 1]</span>
        <p style="font-size: 0.75em;" class="fragment fade-in"><i class="fa fa-lightbulb-o"></i> regarder la base qui est la plus adaptée à la variance de {`$X$`} <i class="fa fa-lightbulb-o"></i></p>

        <br />

        <p class="fragment fade-in" style="font-size: 0.7em;" >
            "théorème spectral" (Mercer {`$\\Rightarrow$`}) :

            <span style="font-size: 0.9em;">
                {`$$c(s,t) = \\operatorname{cov}\\left[ X(s), X(t) \\right] \\underset {\\textsf{Mercer}}{=} \\sum_{\\mathbb N} c_i \\phi_i(s) \\phi_i(t)$$`}

                {`$$\\int \\phi_k(u) c(u,t) du =c[ \\phi_k ] = c_k \\phi_k \\implies \\sum_{\\mathbb N} c_k = \\int_{K^2} c(s,t) dudt$$`}
            </span>
        </p>

        <br />

        <p class="fragment fade-in" style="font-size: 0.7em;">
            Théorème de Karhunen-Loève : <span style="font-size: 0.7em;">{`$\\boxed{X = \\mu + \\sum_{\\mathbb N} \\langle X-\\mu \\vert \\phi_i \\rangle \\phi_i}$`}</span>
        </p>

    </section>

    <!-- ———————————————————————————————————————— ACP en pratique ————————————————————————————————————————————— -->

    <section id="contexte-ACP-2">
        <h3> <i class="fa fa-flag"></i> ACP Fonctionnelle <i class="fa fa-flag"></i></h3>
        <span style="font-size: 0.7em;">[Partie 2]</span>

        <br />

        <p class="fragment fade-in" style="font-size: 0.7em;" >

            <span style="font-size: 0.9em;">
                {`$$\\mathbb E \\Vert X \\Vert^2_{\\mathbb L^2} = \\int_K \\mathbb E[X^2](u)du < \\infty \\implies  \\sum c_i < \\infty \\implies \\sum able$$`}

                <p style="border: 1px solid black; font-size : 0.5em; margin-left : 15%; margin-right : 15%; padding : 3px" class="fragment fade-in">
                    <i class="fa fa-check"></i>on peut donc réordonner les termes par valeur propre décroissante, afin de sélectionner les composantes les plus informatives
                </p>
            </span>
        </p>

        <p class="fragment fade-down" style="font-size: 0.7em;">on peut maintenant approximer {`$b$`} par {`$b_p = \\displaystyle\\sum_{i=1}^{p} \\beta_i(\\phi) \\phi_i$`}</p>
    </section>
    <section id="contexte-ACP-3">
        <h3> <i class="fa fa-flag"></i> ACP Fonctionnelle <i class="fa fa-flag"></i></h3>
        <span style="font-size: 0.7em;">[Partie 3]</span>
        <p style="font-size: 0.75em;"><i class="fa fa-cogs"></i> la pratique <i class="fa fa-cogs"></i></p>
        <p class="fragment fade-in" style="font-size: 0.7em;">
            en se rappelant le <a href="#contexte-model">modèle</a> : {`$Y = \\mathbb E[Y] + \\sum_{i \\geq 1} \\beta_i \\langle X - \\mathbb E [X] \\vert \\phi_i \\rangle_{\\mathbb L^2} + \\varepsilon$`}
        </p>

        <p class="fragment fade-in" style="font-size: 0.7em;"> on observe {`$D = \\left(Y_i[m], T_i[m], X_i[m] = X_i(T_i[m])\\right)_{\\begin{array}{l}i \\in ⟦ 1,n ⟧ \\\\ m \\in  ⟦ 1,M_i ⟧ \\end{array}}$`} <br />

            {`$$
            D
            \\overset{①}{\\rightarrow} \\hat X
            \\overset{②}{\\rightarrow} \\hat \\mu
            \\overset{③}{\\rightarrow} \\hat c
            \\overset{④}{\\rightarrow} \\hat \\phi
            \\overset{⑤}{\\rightarrow} \\langle \\, \\hat x - \\hat \\mu \\, \\vert \\, \\hat \\phi \\, \\rangle
            \\overset{⑥}{\\rightarrow} \\hat \\beta
            $$`}

        </p>

        <p class="fragment fade-in" style="font-size: 0.7em;">
            <br />
            <i class="fa fa-cogs"></i>
            <span style="font-size: 0.7em;"> {`$\\boxed{\\hat b_p = \\displaystyle\\sum_{i=1}^{p} \\beta_i(\\hat \\phi) \\hat \\phi_i  = P^\\perp_{F_p(\\hat \\phi)}( \\, b \\, )}$`}</span>
            <i class="fa fa-cogs"></i>
            <span style="font-size: 0.7em;">
                {`$\\underset {\\textsf{Moindres Carrés}}\\longrightarrow \\hat \\beta(\\hat \\phi) = \\begin{bmatrix} \\vdots \\\\ \\hat \\beta^{LS}_i(\\hat \\phi) \\\\ \\vdots \\end{bmatrix}$`}
            </span>
        </p>

        <aside class="notes">
            <a href="#contexte-model">retour au modele</a>
        </aside>
    </section>

    <!-- ————————————————————————————————————— ACP Questions ———————————————————————————————————— -->

    <section id="contexte-ACP-4">

        <i class="fa fa-check"></i>
        <strong>{`$\\phi$`} représente bien X
        </strong>
        <p class="fragment fade-in">
            <strong>
                <i class="fa fa-warning"></i>
                <!-- <i class="fa fa-arrow-right"></i>  -->
                et {`$b$`} ?
            </strong>
        </p>
        <p class="fragment fade-in">
            <strong>

                <i class="fa fa-warning"></i>
                <!-- <i class="fa fa-arrow-right"></i>  -->
                interactions entre {`$b$`} (et donc {`$Y$`}) et {`$X$`} ?
                <br />({`$Y = a + \\int bX + \\varepsilon$`})
            </strong>
        </p>

    </section>

</section>
