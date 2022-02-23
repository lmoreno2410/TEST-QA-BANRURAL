Se lograron detectar dos fallos de programacion comunes.

1.
Se identifico que hacia falta un punto “.” En la clase low0rHi

//Codigo con error lowOrHi
  let randomNumber = Math.random() * 10;

  const ATTEMPS = 5;
  const guesses = document.querySelector('.guesses');
  const lastResult = document.querySelector('.lastResult');
  const lowOrHi = document.querySelector('lowOrHi');
  const guessSubmit = document.querySelector('.guessSubmit');
  const guessField = document.querySelector('.guessField');

//Codigo con la solucion
  let randomNumber = Math.random() * 10;

  const ATTEMPS = 5;
  const guesses = document.querySelector('.guesses');
  const lastResult = document.querySelector('.lastResult');
  const lowOrHi = document.querySelector('.lowOrHi');
  const guessSubmit = document.querySelector('.guessSubmit');
  const guessField = document.querySelector('.guessField');

2.
Se identifico minisculas en ves de mayusculas en addEventListener

//Codigo con error minisculas en addEventListener

  guessSubmit.addeventListener('click', checkGuess);

  function setGameOver() {
	  guessField.disabled = true;
	  guessSubmit.disabled = true;
	  resetButton = document.createElement('button');
	  resetButton.textContent = 'Comienza un nuevo juego';
	  document.body.appendChild(resetButton);
	  resetButton.addeventListener('click', resetGame);
  }

  //Codigo con la solucion

    guessSubmit.addEventListener('click', checkGuess);

    function setGameOver() {
	  guessField.disabled = true;
	  guessSubmit.disabled = true;
	  resetButton = document.createElement('button');
	  resetButton.textContent = 'Comienza un nuevo juego';
	  document.body.appendChild(resetButton);
	  resetButton.addEventListener('click', resetGame);
  }

