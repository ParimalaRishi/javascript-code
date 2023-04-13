# javascript-code
function fizzBuzzPhone(phoneNumber) {
  // Calculate the sum of the digits in the phone number
  const phoneSum = phoneNumber
    .toString()
    .split('')
    .reduce((sum, digit) => sum + parseInt(digit), 0);

  // Loop from 1 to the sum of the digits in the phone number
  for (let i = 1; i <= phoneSum; i++) {
    // Check if the number is divisible by 4 and/or 5
    const isDivisibleBy4 = i % 4 === 0;
    const isDivisibleBy5 = i % 5 === 0;

    // Print FizzBuzz if divisible by both, Fizz if divisible by 4, Buzz if divisible by 5, and the number otherwise
    if (isDivisibleBy4 && isDivisibleBy5) {
      console.log('FizzBuzz');
    } else if (isDivisibleBy4) {
      console.log('Fizz');
    } else if (isDivisibleBy5) {
      console.log('Buzz');
    } else {
      console.log(i);
    }
  }
}
