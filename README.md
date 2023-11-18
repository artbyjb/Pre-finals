<!DOCTYPE html>
<html>
    <head>
        <body>
            <form id = "primeForm">
                Enter a number:
            <input type="number" id="num" name="num" required><br><br>
            <input type="submit" value="Generate Prime Numbers">
            </form>
        </body>
        <script>
           function analyzeNumber(){
            const number = parselnt(documment.getElementById("numberInput").value);

            let isPrime = true;
            if(number <= 1){
                isPrime = false;
            }else{
                for(let i = 2; i <= Math.sqrt(number);i++){
                    if(number % i === 0){
                        isPrime = false;
                        break;
                    }
                }
            }
            
            const isOdd = number % 2 !== 0;
      const isEven = number % 2 === 0;

      const resultElement = document.getElementById('result');
      if (isPrime) {
        resultElement.textContent = number +' is prime. '; 
      } else {
        resultElement.textContent = number +' is not prime. ';
      }

      if (isOdd) {
        resultElement.textContent += number +' is odd. ';
      } else {
        resultElement.textContent += number +' is even. ';
      }
    }
  </script>
        

           }
        </script>
    </head>

</html>
