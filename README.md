# create-source-code-with-chatgpt

## TypeScript
```
Please write source code as 

If you have any questions, please ask me.

## Does and donts
- use typescript
- use async/await style
- use allow style
- don't use `as` and `any`
- don't put any comments in source code
- use string literal when we use it.each for parameterized test




## Current file contents
 
```

### Update classes
```
Please implement the content of TODO for the following code. 
If other file contents are needed, please list the required file paths before implementation.

### Current source code

```


### Define mock and usecase for unit test for usecase

```
Please define function to return instance of useCase and mock repositories used by usecase.

## Specification
- mock repository
    - define function for each repository .
    - define variable wity type repository.
    - return object after wrap each method with `jest.fn`
    - don't return repository type because we can't use mock function.
    - implement all returning value for each mock. 
        - don't use jest `jest.fn()`
    - Please explicitly specify the data types.
    - Don't use any

- useCase
    - instanciate with mock repositories

## Template
  const createUseCaseAndMockRepositories = () => {
    const {repositoryName} = createMock{repositoryName}();
    const useCase = new {useCaseName}UseCase({repositoryName});
    return {
      {repositoryName},
      useCase,
    };
  };
  const createMock{repositoryName} = () => {
    const repository: {repositoryName} = {
      find: async (_path: string): Promise<EntityDefinition[]> => {
        return [];
      },
    };
    return {
      find: jest.fn((path: string) => repository.find(path)),
    };
  };


## Example
  const createUseCaseAndMockRepositories = () => {
    const entityDefinitionRepository = createMockEntityDefinitionRepository();
    const useCase = new GetDefinitionByPathUseCase(entityDefinitionRepository);
    return {
      entityDefinitionRepository,
      useCase,
    };
  };
  const createMockEntityDefinitionRepository = () => {
    const repository: EntityDefinitionRepository = {
      find: async (_path: string): Promise<EntityDefinition[]> => {
        return [];
      },
    };
    return {
      find: jest.fn((path: string) => repository.find(path)),
    };
  };

## Interface of target usecase class


## Current file contents



```

### create unit test for usecase
```
Please write unit test for useCase class.

## Specification
- Path of test file is `./{UseCaseFileName}.test.ts` in the same directory.
- Please assert each values. (Only toHaveBeenCalled is not enough)
- Please write all assertions in this case.
- Don't put any comments.
- Use always '2000-01-01T00:00:00Z' as current date time.

## Template
//./src/path/to/file
describe('GetSampleUseeCase', () => {
  describe('execute', () => {
    it('should success', async () => {

      const {useCase, dateTimeRepository} = createUseCaseAndMockRepositories()
      const res = useCase.execute()

  })
  const createUseCaseAndMockRepositories = () => {
    const dateTimeRepository = createMockDateTimeRepository();
    ... 
  }
})


## UseCase class

```




### unit test of function
```
Please write unit test for 

If you have any questions, please ask me.

## Does and donts
- use typescript
- use async/await style
- don't put any comments in source code
- use string literal when we use it.each for parameterized test


## Current file contents
 

```


## Create Tests for repository
### Test cases
```
Please listup all test cases for this class.

## Target class
```

### Implement
```
Perfect!!
Please implement all testcases inside this template.

## DOs and DONTs
- check every values of response.
- get content and check values after create/update/delete. 
- don't use mock. server is working, so please use real server.


## Template
```

## README
### npm module
1. Define template
```
What does a great README template look like for a repository on github?
```

1. Write
```
Perfect!!!
Could you please write a fantastic README for this npm module?

## License
MIT

## Usage of this npm module


## current README

## package.json

```
or 
```
Could you please write a fantastic README for this npm module includes below?

- Project Name
- Badges
- Project Description
- Installation
- Usage
- Contributing
- License
- Authors
- Acknowledgements
- FAQs
- Troubleshooting
- Roadmap

## License
MIT

## Usage of this npm module


## current README

## package.json



```

1. Output shell
```
Thank you!
Please output shell script to write this README.md.

```
