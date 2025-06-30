Sistema Inteligente de Detecção de Tumores Cerebrais com Prontuário Médico Automatizado

2. Resumo
Este projeto visa o desenvolvimento de uma solução computacional completa, utilizando uma arquitetura fullstack, para detecção automatizada de tumores cerebrais a partir de imagens de ressonância magnética. A aplicação, baseada em uma API Flask no backend e React no frontend, integra um modelo de visão computacional (YOLO) para identificação precisa de tumores e geração de relatórios médicos em PDF com base na detecção.

3. Objetivos
3.1 Objetivo Geral
Desenvolver uma aplicação fullstack com capacidade de:
    • Detectar tumores cerebrais em imagens de exames médicos
    • Classificar os tipos de tumores
    • Gerar um prontuário médico personalizado automaticamente
3.2 Objetivos Específicos
    • Treinar ou utilizar um modelo YOLO para detecção de tumores.
    • Implementar endpoints RESTful com Flask.
    • Criar uma interface web responsiva com React.
    • Integrar frontend e backend via API.
    • Automatizar a geração de relatórios em PDF com dados personalizados do paciente.

4. Tecnologias Utilizadas
4.1 Backend (Flask)
    • Linguagem: Python 3.10+
    • Framework: Flask
    • Detecção: YOLOv5 (Ultralytics)
    • Banco de Dados: SQLite com SQLAlchemy
    • PDF: ReportLab
4.2 Frontend (React)
    • Linguagem: TypeScript
    • Bibliotecas: React Context API, Fetch API
    • Estilização: CSS Modules/Tailwind (opcional)
4.3 Infraestrutura
    • Execução local com suporte para Replit ou Docker
    • Upload de imagens e armazenamento de relatórios em disco

5. Funcionalidades Implementadas
5.1 Cadastro e Login
    • Registro de usuários com criptografia de senha (bcrypt/werkzeug)
    • Login com validação de credenciais
5.2 Upload de Imagens
    • Envio de imagens de ressonância via formulário web
    • Conversão e redimensionamento da imagem para o modelo
5.3 Detecção com YOLO
    • Detecção e classificação automática:
        ◦ pituitary_tumor
        ◦ glioma_tumor
        ◦ meningioma_tumor
        ◦ no_tumor
5.4 Geração de PDF
    • Diagnóstico automático baseado na classe detectada
    • Recomendações específicas conforme o tipo de tumor
    • Geração de PDF com nome do paciente, data e médico fictício

6. Fluxo do Sistema
    1. O usuário acessa o frontend React e faz login
    2. Realiza o upload de uma imagem de exame
    3. O backend processa a imagem e detecta a classe
    4. A resposta é retornada em JSON
    5. Se for o endpoint com PDF, um relatório é salvo na pasta reports/
    6. O frontend exibe o resultado e permite baixar o PDF

7. Estrutura dos Endpoints da API
Endpoint	Método	Descrição
/	GET	Testa se a API está no ar
/auth/register	POST	Cria um novo usuário
/auth/login	POST	Realiza login
/upload	POST	Realiza upload de imagem para detecção
/uploadwithpdf	POST	Upload + detecção + geração de PDF

8. Resultados Obtidos
    • A aplicação detecta corretamente os tumores com imagens bem posicionadas
    • Relatórios gerados contêm dados realistas e completos
    • Todo o fluxo (cadastro → upload → resultado → relatório) é funcional

9. Conclusão
O projeto demonstra a integração bem-sucedida de IA, backend e frontend em uma aplicação médica interativa. Ele tem potencial para evoluir para uma ferramenta de apoio ao diagnóstico em ambientes reais, com futuras melhorias como:
    • Integração com banco de imagens PACS
    • Upload múltiplo e análise em lote
    • Geração de histórico clínico
    • Armazenamento em nuvem dos relatórios



10. Referências
    • Ultralytics YOLOv5: https://github.com/ultralytics/yolov5
    • Flask: https://flask.palletsprojects.com
    • ReportLab: https://www.reportlab.com
    • Projeto base: https://github.com/gabieluffy/trabalhoyolo.git
