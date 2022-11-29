<script>
    // @ts-nocheck
    import users from "../assets/users.json";
</script>

<main>
    <div class="container-produtos">
        {#each users as user (user.id)}
            <div class="produto">
                <h4>Nº: {user.id}</h4>
                <div class="imagem-div">
                    <img class="imagem" src={user.imagem} alt="" />
                </div>
                <div class="itens-name-valor">
                    <h2>{user.name}</h2>
                    <h2>Valor R$: {user.valor}</h2>
                </div>
                <a href={user.link} target="_blank" rel="noreferrer noopener"> 
                    <button > Comprar  </button>
                </a>
            </div>
        {/each}
    </div>
</main>

<style>
    
    @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@500&family=Roboto:wght@300;400&display=swap');
    h4,h2{
        margin: 0%;
        margin-top: 2px;
    }

    .container-produtos {
        display: flex;
        
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
        font-family: 'Oswald', sans-serif;
        width: 185px;
        font-size: 0.9rem;
        color: #ee4d2d;
    }

    .imagem-div {
        border: solid 2px #000;
        margin: 5px;
        width: 200px;
        height: 200px;
    }
    .imagem {
        margin-top: 5px;
        height: 95%;
        width: 95%;
    }
    button {
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: 'Rboto', sans-serif;
        font-size: 1.1rem;
        background: #ee4d2d;
        color: #000;
        margin: 10px;
        height: 2rem;
        width: 8rem;
    }


</style>
