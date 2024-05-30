<header>
    <nav>
        <img src="/images/tsv-logo.svg" alt="">
        <div class="telefon">
            <img class="phone" src="/images/phone.svg" alt="">
            <a href="tel:+4991948208">+49 9194 8208</a>
        </div>
        
    </nav>
</header>


<style>
    header{
        width: 100%;
        margin: auto;
        z-index: 10;
        position: absolute;

        display: flex;
        justify-content: center;
        align-items: center;
    }

    nav{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-top: 2rem;
        width: 90%;
    }

    .telefon{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 10px;
        transition: all 200ms ease-out;
    }

    .telefon:hover{
        transform: scale(0.97);
    }

    .phone{
        width: 40px;
    }

    img{
        width: 100px;
    }

    a{
        color: white;
    }
</style>