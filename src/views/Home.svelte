<script>
    // @ts-nocheck

    import users from "../assets/users.json";
</script>

<header />

<main>
    <div class="container-produtos">
        {#each users as user (user.id)}
            <div class="produto">
                <div class="imagem-div">
                    <img class="imagem" src={user.imagem} alt="" />
                </div>
                <div class="itens-name-valor">
                    <h2>{user.name}</h2>
                    <h2>Valor R$: {user.valor}</h2>
                </div>
                <button> Comprar </button>
            </div>
        {/each}
    </div>
</main>

<style>
    .container-produtos {
        display: flex;
        width: 1300px;
        background: #ee4d2d;
        flex-wrap: wrap;
        justify-content: center;
    }

    .produto {
        font-family: Inter, Avenir, Helvetica, Arial, sans-serif;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: 8px;
        border-radius: 5px;
        background: #fff;
    }

    .itens-name-valor {
        width: 160px;
        font-size: 0.9rem;
        border-radius: 8px;
        margin: 5px;
        color: #ee4d2d;
    }

    .imagem-div {
        width: 200px;
        height: 200px;
    }
    .imagem {
        margin-top: 10px;
        height: 100%;
        width: 100%;
    }
    button {
        font-family: sans-serif;
        font-size: 1.1rem;
        background: #ee4d2d;
        color: #000;
        margin: 10px;
    }

    @media screen and (max-width: 400px) {
        .container-produtos {
            width: 290px;
        }
        .imagem-div {
            width: 200px;
            height: 200px;
        }
    }
</style>
