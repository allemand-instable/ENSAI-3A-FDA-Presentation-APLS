<!-- ———————————————————————————————————    PLS     ———————————————————————————————————————— -->

<section id="PLS">
    <section id="contexte-PLS-gigachad" data-background-image="img/gigachad_by_haesch_dfbedkv.gif" data-background-opacity="0.4">
        <h1>LA PLS FONCTIONNELLE</h1>
        une vraie technique de GigaChad
    </section>
    <section id="PLS-non-fonctionnelle">
        <h2>mini rappel : PLS (non fonctionnelle)</h2>

        <ul style="font-size: 0.7em;" class="fragment fade-in">
            <li>trouver le sous espace de l'espace engendré par {`$X$`} qui explique le mieux la variance de l'espace engendré par {`$Y$`}</li>

        </ul>
        <ul style="font-size: 0.7em;" class="fragment fade-in">
            <li>on projette {`$X$`} et {`$Y$`} dans un nouvel espace</li>

            {`$\\longrightarrow$`} "latent space" [variable latente | latin : lateo - caché]
        </ul>

    </section>

    <!-- —————————————————————————————————————————— PLS Y chapeau ——————————————————————————————————————————— -->

    <section id="PLS-Y-hat" style="font-size: 0.7em;">

        <h2>comme vu précédemment</h2>

        <p>
            {`$$Y =
            \\underset{
            \\mathbb E [Y \\vert X = x]
            \\underset{\\textsf{notation}}{\\equiv}
            m(x)
            }
            {
            \\boxed{
            \\mathbb E[Y] + \\langle X - \\mathbb E [X] \\vert \\, b \\, \\rangle_{\\mathbb L^2}
            }
            }
            + \\varepsilon
            $$`}

            note : sur la base {`$\\underset{\\Vert \\cdot \\Vert}{\\perp}$`} {`$\\psi$`} de {`$\\mathbb L^2$`} : {`$b = \\sum\\limits_{i\\geq 1} \\langle b \\vert \\psi_i \\rangle \\psi_i$`}
        </p>

        <p class="fragment fade-in">
            on approxime en projetant sur {`$F_p(\\psi)$`}

            {`$$\\hat Y_p^{[\\psi]}
            =
            \\underset{
            \\widehat {\\mathbb{E}}_{p}^{[\\psi] }[Y | X=x]
            \\underset{\\textsf{notation}}{\\equiv}
            \\hat m_{p}^{[\\psi]}(x)
            }
            {\\boxed{\\mathbb E[Y] + \\sum_{i = 1}^{\\color{green}{p}} b_i \\langle X - \\mathbb E [X] \\vert \\psi_i \\rangle_{\\mathbb L^2}}} + \\varepsilon$$`}
        </p>

    </section>

    <!-- ——————————————————————————————————————— PLS Problème de minimisation —————————————————————————————————————————————— -->

    <section id="PLS-pb-min" style="font-size: 0.6em;">

        <h2>Problème de minimisation</h2>

        <span class="fragment fade-down">
            <h4>notation</h4>

            {`$$\\langle f \\vert g \\rangle_{c( \\cdot , \\cdot )} \\underset{\\textsf{notation}}{\\equiv} \\int_{K^2}f(s)c(s,t)g(t) \\, ds \\, dt$$`}

            {`$$\\Vert \\cdot \\Vert^2_{c(\\cdot, \\cdot)} : \\begin{array}{ccc} \\mathcal C^0(K) & \\longrightarrow & \\mathbb R_+ \\\\ f & \\longmapsto & \\int_{K^2} f(s) c(s,t) f(t) \\, ds \\, dt \\end{array}$$`}
        </span>

        <span class="fragment fade-down">

            <h4>expression du problème de minimisation</h4>
            <p>
                {`$$
                \\begin{align}
                (\\hat \\psi_i^*)_{1,p}
                &=
                \\underset{ \\begin{array}{c}\\psi_p \\\\ \\langle \\psi_i \\vert \\psi_p \\rangle_{c(\\cdot , \\cdot)} = 0 \\\\ \\Vert \\psi_p \\Vert = 1 \\end{array} } {\\operatorname{argmin}}
                \\left[
                \\underset{(\\psi_i)_{1,p-1}} {\\operatorname{argmin}}  \\operatorname{COV}\\left(
                \\underset{\\hat \\varepsilon_{p-1}^{[\\psi]}}{\\boxed{Y - \\hat m_{p-1}^{[\\psi]}(x)}} \\,
                ,
                \\, \\langle X \\vert \\psi_p \\rangle \\right)
                \\right]
                \\end{align}
                $$`}
            </p>
        </span>

        <p class="fragment fade-down"> <i class="fa fa-lightbulb-o"></i> {`$\\approx$`} comme en projection-pursuit <i class="fa fa-lightbulb-o"></i> </p>
    </section>

    <!-- ————————————————————————————————————————————————————————————————————————————————————— -->

    <!-- ————————————————————————————————————————————————————————————————————————————————————— -->

    <section id="PLS-theorie-probleme" style="font-size: 0.8em;">

        <p> la PLS n'est pas un nouveau concept </p>

        <p> elle est était déjà utilisée et même en FDA</p>

        <p
            class="fragment fade-down"
            > <i class="fa fa-warning"></i> <strong>MAIS</strong> sans preuve rigoureuse <br> {`$\\rightarrow$`} consistance <br> {`$\\rightarrow$`} vitesse de convergence</p>

    </section>

    <section id="PLS-graph-non-annote">
        <img src="img/graph1_non_annote.jpeg" style="height: 8em;" alt="">

        <img src="img/graph2_non_annote.jpeg" style="height: 7em;" alt="">
    </section>

    <!-- ————————————————————————————————————————————————————————————————————————————————————— -->

    <section id="PLS-apport-du-papier">

        apport de ce papier {`$\\longrightarrow$`} le développement théorique de la PLS Fonctionnelle

        <br>
        <br>

        <p class="fragment fade-down">
            <i class="fa fa-question-circle"></i> comment <i class="fa fa-question-circle"></i>
        </p>

        <br>
        <br>

        <p class="fragment fade-down">
            en travaillant sur un objet plus simple et aux propriétés de convergence équivalentes
        </p>

    </section>

</section>
