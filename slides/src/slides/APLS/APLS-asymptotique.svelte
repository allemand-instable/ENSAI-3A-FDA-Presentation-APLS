<section id="APLS-asymptotique">

    <section id="APLS-asymptotique-">

        <h1>Résultats Asymptotiques</h1>
    </section>

    <section>

        {`$$\\hat c = c + \\frac 1 {\\sqrt n} \\overset{\\color{blue}{[X_i \\, \\mu]}}{\\underset{\\mathbb P}{\\mathcal O}(1)} + \\frac 1 n \\overset{\\color{blue}{[\\overline X \\, \\mu]}}{\\underset{\\mathbb P}{\\mathcal O}(1)}$$`}

        {`$$\\hat c[b] = c[b] = \\frac 1 {\\sqrt n} \\overset{\\color{blue}{[X_i \\, Y_i \\, \\mu]}}{\\underset{\\mathbb P}{\\mathcal O}(1)} + \\frac 1 n \\overset{\\color{blue}{[\\overline X \\, \\overline Y \\, \\mu]}}{\\underset{\\mathbb P}{\\mathcal O}(1)}$$`}

        {`$$\\hat c^i[b] = c^i[b] + \\underset{\\mathbb P}{\\mathcal O}( \\frac 1 {\\sqrt n})$$`}


    </section>

    <section>

        <p class="fragment semi-fade-out">

            {`$$\\sqrt n (\\hat h_{ij} - h_{ij}) \\sim \\mathcal N(0, \\sigma_{ij}^2)$$`}
        </p>

        <p class="fragment fade-in-then-semi-out">

            {`$$\\Vert \\hat c [b] - (c[b] + \\frac \\varepsilon {\\sqrt n}) \\Vert_\\infty = \\underset{\\mathbb P}{\\mathcal O}(n^{-1})$$`}

        </p>

        <p class="fragment fade-in">

            {`$$\\Vert \\hat k - k \\Vert = \\underset{\\mathbb P}{\\mathcal O}( \\frac{1 + \\Vert k \\Vert}{n^{1/2} \\lambda_{min}(H_p)} + \\frac{1}{n \\lambda_{min}(H_p)^3} )$$`}
        </p>

    </section>

    <section style="font-size: 0.7em;">
        <p>

            {`$$\\Vert \\hat k - k \\Vert = \\underset{\\mathbb P}{\\mathcal O}( \\frac{1 + \\Vert k \\Vert}{n^{1/2} \\lambda_{min}(H_p)} + \\frac{1}{n \\lambda_{min}^3(H_p)} )$$`}
        </p>

        <p>
            {`$$\\boxed{

            \\begin{array}{ccc}
            \\operatorname{dim} < \\infty & & \\operatorname{dim} = \\infty
            \\\\
            \\textsf{non sing} & & \\textsf{sing}
            \\\\
            \\lambda_{min}(H_p) & \\xrightarrow[p \\rightarrow \\infty]{} & \\lambda_{min}(H) = 0
            \\end{array}
            }
            $$`}
        </p>

        <p class="fragment fade-down">
            {`$\\implies$ on a besoin que $n^{1/2} \\lambda_{min}(H_p) \\xrightarrow[n \\rightarrow \\infty]{} \\infty$`}

            <br><br>

            ie {`$p(n) \\rightarrow \\infty$ à une vitesse $\\leq \\sqrt n$`}
        </p>
    </section>

    <section style="font-size: 0.7em;">

        {`$$n^{-1/2} \\lambda_{min}(H_p) \\Vert k \\Vert + \\frac{1}{n \\lambda_{min}^3(H_p)} \\xrightarrow[n \\rightarrow \\infty]{} 0$$`}

        {`$$\\Downarrow$$`}

        {`$$\\mathbb E \\left[ \\left\\{\\hat m_p(X) - m(X) \\right\\}^2 | X_{1:n} \\right] = \\underset{\\mathbb P}{\\mathcal O}( \\frac{1 + \\Vert k \\Vert}{n^{1/2} \\lambda_{min}(H_p)} + \\frac{1}{n \\lambda_{min}^3(H_p)} )$$`}

    </section>

</section>
