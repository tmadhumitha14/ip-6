# ip-6
#1
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dynamic List with jQuery</title>
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script> 
<style>
    
    body {
        font-family: Arial, sans-serif;
    }
    #list-container {
        margin-top: 20px;
    }
</style>
</head>
<body>
<h1>Dynamic List with jQuery</h1>
<form id="form">
    <input type="text" id="item" placeholder="Enter an item">
    <button type="button" id="addBtn">Add Item</button>
</form>
<div id="list-container">
    <ul id="item-list"></ul>
</div>

<script>
    $(document).ready(function() {
        $('#addBtn').click(function() {
            var newItemValue = $('#item').val().trim(); 

            if (newItemValue !== '') { 
                
                $('#item-list').append('<li>' + newItemValue + '</li>');

                
                $('#item').val('');
            } else {
                alert('Please enter an item!');
            }
        });
    });
</script>
</body>
</html>

#2
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Count Consonants</title>
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
</head>
<body>
<h1>Count Consonants</h1>
<label for="inputText">Enter a string:</label>
<input type="text" id="inputText">
<button id="countBtn">Count Consonants</button>
<div id="result"></div>

<script>
    $(document).ready(function() {
        $('#countBtn').click(function() {
            var inputString = $('#inputText').val().toLowerCase();  
            var consonantCount = 0;
            var consonants = 'bcdfghjklmnpqrstvwxyz';

            
            for (var i = 0; i < inputString.length; i++) {
                
                if (consonants.indexOf(inputString[i]) !== -1) {
                    consonantCount++;
                }
            }

           
            $('#result').text('Number of consonants: ' + consonantCount);
        });
    });
</script>
</body>
</html>
