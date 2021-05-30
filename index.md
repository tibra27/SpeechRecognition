
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1"
      crossorigin="anonymous"
    />
    <title>Speech To Text</title>
  </head>
    
  <style>
    

    .words {
      max-width: 500px;
      margin: 50px auto;
      background: white;
      border-radius: 5px;
      box-shadow: 10px 10px 0 rgba(0,0,0,0.1);
      padding: 1rem 2rem 1rem 5rem;
      background: -webkit-gradient(linear, 0 0, 0 100%, from(#d9eaf3), color-stop(4%, #fff)) 0 4px;
      background-size: 100% 3rem;
      position: relative;
      line-height: 3rem;
    }
    
    .words:before {
      content: '';
      position: absolute;
      width: 4px;
      top: 0;
      left: 30px;
      bottom: 0;
      border: 1px solid;
      border-color: transparent #efe4e4;
    }
  </style>
  <body class="container pt-5 bg-dark">
    <div class="mt-4" id="div_language">
      <h2 class="mb-3 text-light">Select Language</h2>
      <select class="form-select bg-secondary text-light" id="select_language" onchange="updateCountry()"></select>
      <select class="form-select bg-secondary text-light mt-2" id="select_dialect"></select>
    </div>
	<div class="words">
    <div class="p-3" >
      <span id="final"></span>
      <span id="interim" ></span>
    </div>
	</div>
    <div class="mt-4">
      <button class="btn btn-success" id="start">Start</button>
      <button class="btn btn-danger" id="stop">Stop</button>
      <p id="status" class="lead mt-3 text-light" style="display: none">Listenting ...</p>
    </div>
	<script src="./language.js"></script>
	<script src="./speechRecognition.js"></script>
  
  </body>

</html>
