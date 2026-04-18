# README

## Integrantes
* Alvino Mainette Santos
* Amanda Marcarini Cezanhock
* Thalys Cestari Thouzo

## Descrição do tema escolhido
O NutriFlow é um sistema de gestão de nutrição hospitalar desenvolvido para otimizar o controle de dietas, pacientes e profissionais de saúde dentro de um ambiente clínico. A proposta central do projeto é garantir que a prescrição alimentar seja feita de forma segura, automatizada e alinhada às restrições individuais de cada paciente, reduzindo riscos e melhorando a qualidade do atendimento.

Com base no código apresentado, o sistema foi estruturado utilizando conceitos fundamentais de programação orientada a objetos, como herança, polimorfismo e encapsulamento, permitindo representar de forma organizada os diferentes papéis dentro do hospital. A hierarquia começa com a classe genérica Pessoa, evolui para FuncionárioHospital e chega ao Nutricionista, que possui responsabilidades específicas como validar acesso ao sistema e prescrever dietas. Essa estrutura reflete o funcionamento real de uma equipe hospitalar, onde diferentes níveis de responsabilidade coexistem.

O NutriFlow também se destaca pelo uso de DTOs (Data Transfer Objects) para representar pacientes e dietas, garantindo uma separação clara entre dados e regras de negócio. Os pacientes possuem informações como quarto, restrições alimentares e dieta atual, enquanto as dietas incluem calorias e ingredientes — elementos essenciais para decisões clínicas.

Um dos pontos mais importantes do sistema é a implementação de regras de negócio voltadas à segurança do paciente. Antes de uma dieta ser prescrita, o sistema verifica automaticamente se há conflito entre os ingredientes da dieta e as restrições alimentares do paciente. Caso exista alguma incompatibilidade, uma exceção específica é lançada, evitando erros que poderiam comprometer a saúde do paciente. Além disso, há controle de acesso para garantir que apenas nutricionistas válidos e ativos possam realizar prescrições.

Outro aspecto relevante é o gerenciamento centralizado feito pela classe HospitalManager, responsável por cadastrar pacientes e dietas, além de realizar buscas e prescrições. O sistema ainda oferece funcionalidades práticas, como listar pacientes, consultar dietas disponíveis e buscar pacientes com determinadas restrições alimentares, facilitando o trabalho no dia a dia hospitalar.

Por fim, o NutriFlow incorpora boas práticas modernas de desenvolvimento, como tratamento estruturado de exceções, uso de listas e dicionários para armazenamento em memória e uma interface simples baseada em menu interativo. Dessa forma, o projeto não apenas demonstra domínio técnico, mas também apresenta uma solução aplicável a cenários reais, promovendo segurança alimentar, eficiência operacional e apoio à tomada de decisão clínica dentro de hospitais.

## Instruções de como executar o sistema
1. Certifique-se de ter o Python 3.10 ou superior instalado (devido ao uso estrutural de `match/case`).
2. Clone o repositório ou baixe o arquivo `main.py`.
3. Abra o terminal e execute o comando:
   ```bash
   python main.py

## O que achamos mais desafiador na transição para o Python?
O que achamos mais desafiador e interessante na transição das linguagens da família C para o Python foi a mudança de paradigma na declaração de estruturas de dados e na flexibilidade de tipos.

Structs x Dataclasses: No C/C++, definir estruturas para transferir dados de pacientes e dietas exige criação manual de structs e construtores verbosos. No Python, a anotação @dataclass abstraiu a criação do init, permitindo montar os nossos Data Transfer Objects (DTOs) de forma muito enxuta e legível.

Tratamento de Exceções como Regra de Negócio: Em C, validar alergias provavelmente envolveria aninhar vários if/else e retornar códigos de erro (como -1 ou 0). No Python, nós criamos uma classe dedicada RestricaoAlimentarVioladaError. Usando a estrutura completa de try/except/else/finally, conseguimos isolar a regra de negócio do fluxo principal, deixando o código resiliente.

List Comprehensions vs Laços Tradicionais: A busca de pacientes por restrições demonstrou o poder expressivo do Python. Uma filtragem que em C exigiria a alocação de um novo array, um laço for com contadores e verificação de strings, foi resolvida em uma única linha elegante no Python.

   
