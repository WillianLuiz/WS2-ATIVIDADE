# 🛠️ Atividade Prática SPONDEO

Bem-vindos à atividade prática do nosso Workshop de CI/CD para a disciplina de Testes e Manutenção de Software da UFU! 🚀

Este repositório contém uma versão simplificada do motor de validação de vagas do projeto **SPONDEO**. Nós configuramos uma pipeline de Integração Contínua (CI) usando o **GitHub Actions**.

**O Problema:** Nossa equipe sabotou o projeto de propósito! Espalhamos **10 falhas lógicas** na nossa suite de testes unitários. O código de produção diz uma coisa, mas o teste espera outra.

**Sua Missão:** Usar os logs da pipeline de CI para encontrar os bugs, corrigir os testes e conquistar a cobiçada "Pipeline Verde"! ✅

---

## 🎯 Passo a Passo da Dinâmica

Não é necessário clonar o projeto ou instalar o Java na sua máquina! Você pode fazer tudo direto aqui pelo navegador.

* **Passo 1:** Faça o **Fork** deste repositório para a sua conta do GitHub (botão no canto superior direito). Após o fork, vá na aba **"Actions"** do *seu* repositório e clique no botão verde para habilitar os Workflows.
* **Passo 2:** Vá na aba "Actions", selecione "CI - Atividade SPONDEO" na lateral esquerda e clique em **Run workflow** (ou faça qualquer alteração neste README e dê um commit). A pipeline vai rodar e **vai falhar! 🚨**
* **Passo 3:** Clique no ícone de erro (❌), abra o passo chamado `Testes Unitários` e **leia os Logs do Maven**. O CI vai te apontar exatamente qual linha quebrou e o porquê (ex: `expected: "Gupy" but was: "LinkedIn"`).
* **Passo 4:** Navegue até o arquivo `src/main/java/io/github/raphaelmun1z/services/system/VagaServiceTest.java`. Clique no ícone de lápis ✏️ para editar (ou aperte a tecla `.` para abrir o VS Code no navegador). Encontre as falhas lógicas nos `assertThat` ou `verify`, corrija os valores e faça o **Commit**.
* **Passo 5:** Volte na aba Actions e acompanhe a execução. Sua meta é consertar todos os erros até **Conquistar a Pipeline Verde ✅**!

---

## 💡 Dicas de Ouro

1. **Leia os Logs com Atenção:** O CI é o seu melhor amigo. Ele sempre vai te dizer o que ele esperava (`Expected`) e o que realmente chegou (`But was`).
2. **O Efeito "Fail-Fast" do JUnit:** O framework de testes para no *primeiro* erro que encontra dentro de um método. Se você consertar um erro e fizer o commit correndo, a pipeline pode falhar de novo na linha de baixo! **Dica:** Leia o bloco de código inteiro do teste para ver se não há mais de uma sabotagem escondida antes de commitar! 👀

---

### 👨‍💻 Equipe
Desenvolvido para o Workshop de Automação de Pipelines por:
* Caio Soares
* Raphael Muniz
* Ygor Marangoni

Boa sorte! 
