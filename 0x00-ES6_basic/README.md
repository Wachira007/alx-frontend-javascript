0. Modification of:

    function taskFirst to instantiate variables using const
    function taskNext to instantiate variables using let

code:
export function taskFirst() {
  var task = 'I prefer const when I can.';
  return task;
}

export function getLast() {
  return ' is okay';
}

export function taskNext() {
  var combination = 'But sometimes let';
  combination += getLast();

  return combination;
}

1. Modification of the variables inside the function taskBlock so that the variables aren't overwritten inside the conditional block
code:
export default function taskBlock(trueOrFalse) {
  var task = false;
  var task2 = true;

  if (trueOrFalse) {
    var task = true;
    var task2 = false;
  }

  return [task, task2];
}

2. Rewriting the functions to use ES6's arrow syntax of the function add (an anonymus function after)
code:
export default function getNeighborhoodsList() {
  this.sanFranciscoNeighborhoods = ['SOMA', 'Union Square'];

  const self = this;
  this.addNeighborhood = function add(newNeighborhood) {
    self.sanFranciscoNeighborhoods.push(newNeighborhood);
    return self.sanFranciscoNeighborhoods;
  };
}

3. Condense the internals of the following function to 1 line - without changing the name of each function/variable. (done by defining default parameter values for the function parameters.)
code:
export default function getSumOfHoods(initialNumber, expansion1989, expansion2019) {
  if (expansion1989 === undefined) {
    expansion1989 = 89;
  }

  if (expansion2019 === undefined) {
    expansion2019 = 19;
  }
  return initialNumber + expansion1989 + expansion2019;
}

4. Modification of the function to return the number of arguments passed to it using the rest parameter syntax


export default function returnHowManyArguments() {

}

5. Using spread syntax, concatenation of 2 arrays and each character of a string by modifying the function below:
code: (The function is restricted to one line long)

export default function concatArrays(array1, array2, string) {
}

6. Rewriting the return statement to use a template literal so that the substitution of the variables can take place
code:
export default function getSanFranciscoDescription() {
  const year = 2017;
  const budget = {
    income: '$119,868',
    gdp: '$154.2 billion',
    capita: '$178,479',
  };

  return 'As of ' + year + ', it was the seventh-highest income county in the United States'
        / ', with a per capita personal income of ' + budget.income + '. As of 2015, San Francisco'
        / ' proper had a GDP of ' + budget.gdp + ', and a GDP per capita of ' + budget.capita + '.';
}

7. keys and variables are the same 
Modification of function's budget object to simply use the keyname instead.
export default function getBudgetObject(income, gdp, capita) {
  const budget = {
    income: income,
    gdp: gdp,
    capita: capita,
  };

  return budget;
}

