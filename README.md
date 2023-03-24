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
- don't any comments in source code
- use template literal when we use it.each for parameterized test




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
\`\`\`
\`\`\`

## Current file contents



```
