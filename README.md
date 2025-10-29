# AWS_CloudFormation-CodeGirls2025
Documentação e insights sobre a implementação de uma Stack utilizando AWS CloudFormation.

## O que é o AWS CloudFormation?

O AWS CloudFormation é um serviço que permite criar, configurar e gerenciar recursos AWS através de modelos declarativos (YAML/JSON), facilitando a automação e a padronização de infraestruturas em nuvem.

Com o CloudFormation, é possível provisionar, de forma automatizada e reprodutível, recursos como:
- Instâncias EC2
- S3 Buckets  
- VPCs e Subnets  
- Security Groups  
- IAM Roles e Policies  

# Dicas de Utilização do CloudFormation

- Organize seus templates por recurso ou ambiente (ex.: network.yml, storage.yml, compute.yml).
- Evite alterações manuais em recursos criados por CloudFormation — modifique o template e atualize a stack.
- Use parâmetros (Parameters) para tornar seus templates reutilizáveis entre ambientes.
- Documente cada recurso com descrições (Description) para facilitar a manutenção.
- Controle permissões: garanta que seu usuário possua políticas IAM adequadas para criar os recursos desejados.
- Verifique dependências usando a aba Events no console do CloudFormation — ela mostra o que falhou e por quê.

## Etapas da Criação da Stack

Durante o laboratório, o processo de criação da minha Stack seguiu os seguintes passos:

1. **Acesso ao console do CloudFormation**  
   Entrei no painel da AWS e selecionei o serviço CloudFormation. A interface é bem intuitiva e oferece a opção *Create Stack*.

2. **Upload do template YAML**  
   Fiz o upload de um template simples que criei para provisionar um bucket S3 com versionamento ativado.

3. **Configuração dos parâmetros da Stack**
Dei um nome à Stack e segui as etapas padrão sem modificar permissões ou políticas específicas, já que o objetivo era apenas compreender o fluxo de criação.

4. **Implantação e acompanhamento**
Após criar a Stack, acompanhei o status em Events, onde cada recurso é listado conforme é criado. Em poucos segundos, a Stack foi marcada como CREATE_COMPLETE, e pude visualizar o bucket criado diretamente no console do Amazon S3.

5. **Verificação dos recursos**
Confirmei que o bucket havia sido criado com o nome definido e que o versionamento estava habilitado, conforme configurado no template.
