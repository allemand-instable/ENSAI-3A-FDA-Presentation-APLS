<section>
    <section id="APLS-empirique">
        <h1>L'Empirique</h1>
    </section>

    <section>
        {`$$
        \\begin{array}

        \\tilde{m}_p(X) &=& \\mathbb E [Y] &+ \\langle X - \\mu | \\tilde b_p \\rangle
        \\\\

        \\downarrow & & \\downarrow & \\quad \\quad \\downarrow

        \\\\
        \\hat m_p(x) &=& \\overline Y &+ \\langle X - \\hat \\mu | \\hat b_p \\rangle

        \\end{array}
        $$`}
    </section>

    <section>
        <strong>théorème [3.5]</strong>

        {`$$\\min\\limits_k \\mathbb E [ (m(X) - \\tilde m_p^{[c]}(x))^2 ] \\longrightarrow k = H^{-1} \\alpha$$`}

        {`$H = \\begin{bmatrix} \\langle c^{i+1}[b] | c^j[b] \\rangle \\end{bmatrix}_{ij} \\quad$ et $\\quad \\alpha = \\begin{bmatrix} \\vdots \\\\ c^i[b] \\\\ \\vdots \\end{bmatrix}_i$`}
    </section>

    <section>
        {`$$\\hat k = \\hat H^{-1} \\hat \\alpha$$`}
    </section>

    <section style="font-size: 0.6em;">
        <div class="flex-container" style="display: flex;">

            <div style="flex: 1; margin-right: 10px; border: 1.5px solid black;">
                ce qu'on approxime :
                {`$$
                \\begin{array}
                \\hat c(s,t) &
                \\\\
                \\hat c[b] &
                \\\\
                &\\longrightarrow \\hat k
                \\\\
                \\hat c^i[b] &
                \\\\
                \\hat H = [\\hat h_{ij}]_{ij} &
                \\end{array}
                $$`}
            </div>

            <div style="flex: 1; margin-right: 10px; border: 1.5px solid black;" class="fragment fade-in">

                {`$$\\mathbb E \\rightarrow \\frac 1 n \\sum_{i=1}^n$$`}

                {`$$\\hat k = \\underset{k}{\\operatorname{argmin}} \\frac 1 n \\sum_i(Y_i - \\overline Y) - \\sum^p_j k_j \\int(X - \\overline X) \\hat c ^j[b]$$`}

                {`$$\\hat c(s,t) \\frac 1 n \\sum_i (X_i(s) - \\overline X(s))(X_i(t) - \\overline X(t))$$`}

                {`$$\\hat c[b] = \\frac 1 n \\sum_i (X_i - \\overline X)(Y_i - \\overline Y)$$`}

                {`$$\\hat c^{i+1}[b] = \\int \\hat c^i[b](u) \\hat c(u,t) du$$`}

            </div>
        </div>
    </section>

    <section>

        {`$\\longrightarrow$`} contrôler en {`$p$`}

        <br> <br> <br>

        {`$\\longrightarrow$`} contrôler en {`$n$`}
        <br>
        <p class="fragment fade-down">

            {`$\\rightarrow$`} prendre {`$p(n)$`} approprié
        </p>

    </section>
</section>
