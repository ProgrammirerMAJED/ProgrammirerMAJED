<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cacloulator</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Zen+Maru+Gothic:wght@300;400;500;700;900&display=swap" rel="stylesheet">
    
<head>

<style>
    body {
    font-family: 'Montserrat', sans-serif;
    margin: 0;
}

table {
    width: 100%;
    height: 70vh;
    color: white;
    background-color: #7f8fa0;
}

        td {
            width: 25%;
            text-align: center;
            font-size: 24px;
            background-color: #2ecc71;
        }
        td:hover {
            background-color: #77f5ab;
            cursor: pointer;
        }
#resultArea {
    height: 30vh;
    background-color: #34495e;
    color: white;
    font-size: 64px;
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    padding: 24px;
    box-sizing: border-box;
}

#result {
    background-color: #59f5f5;
}

#result:hover {
    background-color: #88f5ac;
}

.highlight {
    background-color: #0066aa;
}

</style>


<script>

    function appendOperation(Operation) {

        document.getElementById('resultArea').innerHTML +=Operation;F
    }

    function a() {
        let container = document.getElementById('resultArea');
        let result = eval(container.innerHTML)
        container.innerHTML = result;
    }

    function deleteLast() {
        let container = document.getElementById('resultArea');
        if(container.innerHTML.endsWith(' ')){
            container.innerHTML=container.innerHTML.slice(0, -3)
        }else{
        container.innerHTML=container.innerHTML.slice(0, -1)
    }
    }

</script>
</head>

<body>

<div id="resultArea">

</div>
    <table>
        <tr>
            <td onclick="appendOperation(' ( ')" class="highlight">(</td>
            <td onclick="appendOperation(' ) ')" class="highlight">)</td>
            <td onclick="appendOperation('')"> </td>
            <td onclick="deleteLast()">DEL</td>
        </tr>
        <tr>
        <td onclick="appendOperation(7)">7</td>
        <td onclick="appendOperation(8)">8</td>
        <td onclick="appendOperation(9)">9</td>
        <td class="highlight"  onclick="appendOperation(' / ')">/</td>
        </tr>

        <tr>
            <td  onclick="appendOperation(4)">4</td>
            <td  onclick="appendOperation(5)">5</td>
            <td onclick="appendOperation(6)">6</td>
            <td onclick="appendOperation('*')" class="highlight">x</td>
        </tr>

        <tr>
            <td  onclick="appendOperation(1)">1</td>
            <td  onclick="appendOperation(2)">2</td>
            <td  onclick="appendOperation(3)">3</td>
            <td  onclick="appendOperation(' + ')" class="highlight">+</td>
        </tr>
                                                                                           
        <tr>
            <td  onclick="appendOperation(0)">0</td>
            <td  onclick="appendOperation('.')">,</td>
            <td onclick="a()" id="result">=</td>
            <td  onclick="appendOperation(' - ')"  class="highlight">-</td>
        </tr>

        

    </table>
 
</body>

</html>
