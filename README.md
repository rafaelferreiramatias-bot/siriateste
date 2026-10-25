
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cultura Síria</title>

<style>
:root {
    --tema: claro;

    --fundo-claro: #f5efe5;
    --superficie-clara: #fffaf2;
    --texto-claro: #302923;
    --primaria-clara: #a83232;
    --verde-claro: #174b35;
    --borda-clara: #e4d5c0;

    --fundo-escuro: #101b18;
    --superficie-escura: #1b2b25;
    --texto-escuro: #f6f0e5;
    --primaria-escura: #ef8880;
    --verde-escuro: #263e32;
    --borda-escura: #3b5044;
}

:root:has(#tema:checked) {
    --tema: escuro;
}

* {
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    line-height: 1.7;

    background-color: var(--fundo-claro);
    color: var(--texto-claro);

    background-color: if(
        style(--tema: escuro):
            var(--fundo-escuro);
        else:
            var(--fundo-claro)
    );

    color: if(
        style(--tema: escuro):
            var(--texto-escuro);
        else:
            var(--texto-claro)
    );

    transition: background-color 0.3s, color 0.3s;
}

#tema {
    position: absolute;
    width: 1px;
    height: 1px;
    opacity: 0;
}

header {
    padding: 35px 20px;
    text-align: center;

    background-color: var(--superficie-clara);
    background-color: if(
        style(--tema: escuro):
            var(--superficie-escura);
        else:
            var(--superficie-clara)
    );

    border-bottom: 4px solid var(--verde-claro);
    border-color: if(
        style(--tema: escuro):
            var(--borda-escura);
        else:
            var(--verde-claro)
    );
}

header h1 {
    color: var(--primaria-clara);
    color: if(
        style(--tema: escuro):
            var(--primaria-escura);
        else:
            var(--primaria-clara)
    );
}

header p {
    margin-bottom: 0;
}

nav {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 20px;
    padding: 15px;

    background-color: var(--verde-claro);
    background-color: if(
        style(--tema: escuro):
            var(--verde-escuro);
        else:
            var(--verde-claro)
    );

    color: white;
}

nav a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

nav a:hover {
    text-decoration: underline;
}

.botao-tema {
    border: 2px solid white;
    border-radius: 25px;
    padding: 8px 15px;
    cursor: pointer;
    color: white;
}

.texto-claro {
    display: none;
}

.texto-escuro {
    display: inline;
}

:root:has(#tema:checked) .texto-claro {
    display: inline;
}

:root:has(#tema:checked) .texto-escuro {
    display: none;
}

main {
    width: min(1100px, 90%);
    margin: 35px auto;
}

.introducao,
.sobre,
.card {
    background-color: var(--superficie-clara);
    background-color: if(
        style(--tema: escuro):
            var(--superficie-escura);
        else:
            var(--superficie-clara)
    );

    border: 1px solid var(--borda-clara);
    border-color: if(
        style(--tema: escuro):
            var(--borda-escura);
        else:
            var(--borda-clara)
    );

    border-radius: 12px;
    padding: 25px;
    margin-bottom: 30px;
}

h2, h3 {
    color: var(--primaria-clara);
    color: if(
        style(--tema: escuro):
            var(--primaria-escura);
        else:
            var(--primaria-clara)
    );
}

.secao-cards > h2 {
    text-align: center;
    margin-bottom: 25px;
}

.cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 22px;
}

.card {
    padding: 0;
    overflow: hidden;
    transition: transform 0.2s;
}

.card:hover {
    transform: translateY(-5px);
}

.card img {
    display: block;
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.card-conteudo {
    padding: 20px;
}

.card-conteudo p {
    color: #716459;
    color: if(
        style(--tema: escuro):
            #c2cec5;
        else:
            #716459
    );
}

.bandeira {
    width: min(300px, 100%);
    margin: 20px auto;
    border: 1px solid #999;
}

.faixa {
    height: 40px;
}

.vermelho {
    background: #ce2028;
}

.branco {
    background: white;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 25px;
}

.preto {
    background: #111;
}

.estrela {
    color: #168447;
    font-size: 25px;
}

footer {
    padding: 25px;
    text-align: center;
    color: white;

    background-color: var(--verde-claro);
    background-color: if(
        style(--tema: escuro):
            var(--verde-escuro);
        else:
            var(--verde-claro)
    );
}

@media (max-width: 600px) {
    main {
        width: 92%;
    }

    nav {
        gap: 12px;
    }

    .introducao, .sobre {
        padding: 20px;
    }
}
</style>
</head>

<body>

<input type="checkbox" id="tema">

<header id="inicio">
    <h1>Cultura Síria</h1>
    <p>História, tradições e sabores do Oriente Médio</p>
</header>

<nav>
    <a href="#inicio">Início</a>
    <a href="#historia">História</a>
    <a href="#cultura">Cultura</a>
    <a href="#bandeira">Bandeira</a>
    <a href="#sobre">Sobre</a>

    <label for="tema" class="botao-tema">
        <span class="texto-escuro">🌙 Tema escuro</span>
        <span class="texto-claro">☀️ Tema claro</span>
    </label>
</nav>

<main>

<section class="introducao" id="historia">
    <h2>Conheça a Síria</h2>
    <p>
        A Síria é um país do Oriente Médio com uma história milenar.
        Sua capital é Damasco, uma cidade conhecida por seu patrimônio
        histórico e cultural.
    </p>
    <p>
        A cultura síria reúne influências de diferentes povos e
        civilizações. Sua identidade aparece na arquitetura, na
        culinária, na música, na literatura e nas tradições familiares.
    </p>
</section>

<section class="secao-cards" id="cultura">
    <h2>Tradições da cultura síria</h2>

    <div class="cards">

        <article class="card">
            <img src="https://images.unsplash.com/photo-1548013146-72479768bada?auto=format&fit=crop&w=900&q=80" alt="Arquitetura histórica">
            <div class="card-conteudo">
                <h3>🏛️ Arquitetura</h3>
                <p>
                    Damasco e Aleppo possuem mercados tradicionais,
                    construções históricas, pátios internos e
                    monumentos que representam diferentes épocas.
                </p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1547592180-85f173990554?auto=format&fit=crop&w=900&q=80" alt="Comida servida à mesa">
            <div class="card-conteudo">
                <h3>🍽️ Gastronomia</h3>
                <p>
                    A culinária síria utiliza grãos, vegetais,
                    azeite e especiarias. Entre os pratos conhecidos
                    estão quibe, tabule, homus e doces tradicionais.
                </p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1600166898405-da9535204843?auto=format&fit=crop&w=900&q=80" alt="Tapete artesanal">
            <div class="card-conteudo">
                <h3>🧵 Artesanato</h3>
                <p>
                    Tecidos, bordados, cerâmicas e trabalhos em
                    madeira mostram técnicas artesanais transmitidas
                    de geração em geração.
                </p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1516280440614-37939bbacd81?auto=format&fit=crop&w=900&q=80" alt="Apresentação musical">
            <div class="card-conteudo">
                <h3>🎶 Música e dança</h3>
                <p>
                    A música tradicional combina instrumentos,
                    canto e ritmos regionais. A dabke é uma dança
                    coletiva presente em diversas celebrações.
                </p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1490730141103-6cac27aaab94?auto=format&fit=crop&w=900&q=80" alt="Paisagem natural">
            <div class="card-conteudo">
                <h3>🌍 Geografia</h3>
                <p>
                    O território sírio inclui áreas costeiras,
                    montanhas, planícies e regiões desérticas.
                    Sua localização influenciou antigas rotas comerciais.
                </p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1511988617509-a57c8a288659?auto=format&fit=crop&w=900&q=80" alt="Pessoas reunidas">
            <div class="card-conteudo">
                <h3>☕ Hospitalidade</h3>
                <p>
                    Receber visitantes, compartilhar refeições
                    e oferecer café ou chá são costumes valorizados
                    em muitas comunidades sírias.
                </p>
            </div>
        </article>

    </div>
</section>

<section class="sobre" id="bandeira">
    <h2> Bandeira da Síria</h2>

    <div class="bandeira" role="img" aria-label="Bandeira síria estilizada">
        <div class="faixa vermelho"></div>
        <div class="faixa branco">
            <span class="estrela">★</span>
            <span class="estrela">★</span>
            <span class="estrela">★</span>
        </div>
        <div class="faixa preto"></div>
    </div>

    <p>
        A bandeira verde, branca e preta com três estrelas vermelhas
        é um símbolo nacional associado à história política síria.
        As bandeiras e seus significados refletem diferentes
        momentos da trajetória do país.
    </p>
</section>

<section class="sobre" id="sobre">
    <h2>Uma cultura de diversidade</h2>
    <p>
        A sociedade síria reúne diferentes comunidades,
        tradições religiosas, expressões artísticas e costumes
        regionais. Essa diversidade faz parte de sua identidade.
    </p>
    <p>
        O árabe é a língua oficial. A cultura síria também se
        destaca pela literatura, pelo artesanato, pela culinária
        e pela importância dos encontros familiares.
    </p>
</section>

</main>

<footer>
    <p>&copy; 2026 — Cultura Síria</p>
    <p>História, arte, gastronomia e tradições.</p>
</footer>

</body>
</html>
