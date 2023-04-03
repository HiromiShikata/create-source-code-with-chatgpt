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

### Define mock and usecase for unit test for usecase

```
Please define function to return instance of useCase and mock repositories used by usecase.

## Specification
- mock repository
    - define function for each repository .
    - define variable wity type repository.
    - return object after wrap each method with `jest.fn`
    - don't return repository type because we can't use mock function.
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
- Don't put any comments.

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
