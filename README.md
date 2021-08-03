# htm-css

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 100%;
        color: #040004;
        line-height: 1.5;
    }

    .content {
        background-color: #FFF;
        width: 720px;
        padding: 20px;
        margin: 20px auto 0 auto;
        box-shadow: 0px 6px 10px;
        border-radius: 5px;
    }

    .row {
        padding: 5px;
    }

    .buttons {
        text-align: center;
    }

    fieldset {
        border-radius: 5px;
        padding: 20px;
        margin-bottom: 20px;
        border-color: #c2cbce;
        box-shadow: 2px 2px 2px #c2cbce;
    }

    legend {
        font-size: 2rem;
        font-weight: bold;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
    }

    label:not([for="casado"], [for="solteiro"], [for="java"], [for="php"], [for="csharp"]) {
        display: inline-block;
        width: 120px;
    }

    input {
        padding: 2px;
        outline: none;
    }

    input[id="nome"],
    input[id="sobrenome"],
    input[id="email"] {
        width: 480px;
    }

    input[id="dtnasc"] {
        width: 180px;
    }

    input[type="text"],
    input[type="date"],
    input[type="number"],
    input[type="email"] {
        border: none;
        border-bottom: 2px solid #c2cbce;
        transition: 0.3s all ease-in-out
    }

    input[type="text"]:focus,
    input[type="date"]:focus,
    input[type="number"]:focus,
    input[type="email"]:focus {
        color: #c9920e;
        font-weight: 600;
        letter-spacing: 1px;
        border-color: #c9920e;
    }

    textarea {
        padding: 10px;
        resize: none;
        outline: none;
        width: 100%;
    }

    input[type="radio"],
    input[type="checkbox"] {
        margin-top: 10px;
        margin-bottom: 10px;
    }

    input::-webkit-outer-spin-button,
    input::-webkit-inner-spin-button {
        -webkit-appearance: none;
        margin: 0;
    }

    input[type="submit"],
    input[type="reset"] {
        padding: 5px 10px;
        background-color: #c9920e;
        border: none;
        border-radius: 5px;
        color: #fff;
        transition: 0.3s all ease-in-out;
    }

    input[type="submit"]:hover,
    input[type="reset"]:hover {
        transform: scale(1.2);
    }

    label[for="java"],
    label[for="csharp"],
    label[for="php"] {
        border: 1px solid #040004;
        border-radius: 5px;
        padding: 10px 15px;
        font-weight: 600;
        margin: 10px 0 10px 0;
        display: inline-block;
        transition: 0.3s all ease-in-out
    }

    input[type="checkbox"]:checked+label {
        background-color: #00d4ff;
        border-color: #00d4ff;
        color: #FFF;
    }

    input[type="checkbox"] {
        display: none;
    }

    label[for="java"]:hover,
    label[for="csharp"]:hover,
    label[for="php"]:hover,
    input[type="submit"],
    input[type="reset"] {
        cursor: pointer;
    }

    body {
        background: rgb(2, 0, 36);
        background: linear-gradient(90deg, rgba(2, 0, 36, 1) 0%, rgba(9, 9, 121, 1) 0%, rgba(0, 212, 255, 1) 100%);
    }
</style>

<body>
    <div class="content">
        <form action="">
            <fieldset>
                <legend>Dados Pessoais</legend>
                <div class="row">
                    <label for="nome">Nome</label>
                    <input type="text" id="nome" name="nome" placeholder="Digite seu nome" autocomplete="off" required>
                </div>
                <div class="row">
                    <label for="sobrenome">Sobrenome</label>
                    <input type="text" id="sobrenome" name="sobrenome" placeholder="Sobrenome" autocomplete="off"
                        required>
                </div>
                <div class="row">
                    <label for="email">E-mail</label>
                    <input type="email" id="email" name="email" placeholder="e-mail" autocomplete="off" required>
                </div>
                <div class="row">
                    <label for="dtnasc">Data de Nascimento</label>
                    <input type="date" id="dtnasc" name="dtnasc">
                </div>
                <div class="row">
                    <label for="">Estado Civil</label>
                    <input type="radio" value="Casado" id="casado" name="estadocivil">
                    <label for="casado">Casado</label>
                    <input type="radio" value="Solteiro" id="solteiro" name="estadocivil">
                    <label for="solteiro">Solteiro</label>
                </div>
                <div class="row">
                    <label for="filhos">Filhos</label>
                    <input type="number" id="filhos" name="filhos" max="10" min="0">
                </div>
                <div class="row"></div>
            </fieldset>
            <fieldset>
                <legend>Dados Profissionais</legend>
                <div class="row">
                    <label for="">Selecione as linguagens que você conhece</label>
                </div>
                <div class="row">
                    <input type="checkbox" id="php" name="php">
                    <label for="php">PHP</label>
                    <input type="checkbox" id="java" name="java">
                    <label for="java">Java</label>
                    <input type="checkbox" id="csharp" name="csharp">
                    <label for="csharp">C#</label>
                </div>
                <div class="row">
                    <label for="sobre">Fale sobre você</label>
                </div>
                <div class="row">
                    <textarea name="sobre" id="sobre" cols="30" rows="5" placeholder="Descreva as suas habilidades"
                        autocomplete="off"></textarea>
                </div>
                <div class="row">
                    <input type="file" accept=".pdf, .docx">
                </div>
            </fieldset>
            <div class="buttons">
                <input type="submit">
                <input type="reset" value="Limpar">
            </div>
        </form>
    </div>
</body>

</html>
