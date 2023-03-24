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
