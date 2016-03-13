Math Factory
========

AngularJS factory that provides properties and methods that describe a question object containing
a random arithmetic question, randomized options and the answer.

========

####Inject into module
```
angular.module('someModule').controller('someController',
  ['$scope', '$MathFactory',
  function($scope, $MathFactory){

    ...

  }
]);

```

####Initialize the question object

```
angular.module('someModule').controller('someController',
  ['$scope', 'MathFactory',
  function($scope, MathFactory){

    MathFactory.loadAdditionQuestions(numberOfQuestions);

  }
]);

```

There are currently four type of questions you can initialize:

```

MathFactory.loadAdditionQuestions(numberOfQuestions)
MathFactory.loadSubtractionQuestions(numberOfQuestions)
MathFactory.loadDivisionQuestions(numberOfQuestions)
MathFactory.loadMultiplicationQuestions(numberOfQuestions)

```

####Get the question

```
angular.module('someModule').controller('someController',
  ['$scope', 'MathFactory',
  function($scope, MathFactory){

    MathFactory.loadAdditionQuestions(numberOfQuestions);

    ...

    $scope.question = MathFactory.getQuestion(numberOfQuestions);

  }
]);

```

An example of the question object returned

```

var question = {
  question: "6 + 2",
  options = ['2', '8', '5', '9'],
  answer: 2
}

```
