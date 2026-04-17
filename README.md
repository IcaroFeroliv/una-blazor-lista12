# LISTA 12🌍

## 👥 Identificação
* **Integrantes da Equipe:** 
    * **Icaro Ferreira de Oliveira** | Curso: Análise e Desenvolvimento de Sistemas (ADS) 
    * **Kaio Robertt Moreira Abreu** | Curso: Análise e Desenvolvimento de Sistemas (ADS) 
* **Instituição:** Centro Universitário UNA
* **Disciplina:** Interação Humano Computador e UX 
* **Professor:** Daniel Henrique Matos de Paiva 
---

## 🧠 Heurísticas de Nielsen Aplicadas
Neste projeto, focamos na implementação de diretrizes de usabilidade para garantir uma experiência fluida:

1.  **Visibilidade do Status do Sistema:** O componente fornece feedback imediato ao usuário. Ao clicar em "Registrar Atividade", o contador de "Total acumulado" e a barra de progresso são atualizados instantaneamente, permitindo que o usuário saiba que sua ação foi processada pelo sistema.
2.  **Consistência e Padronização:** Utilizamos a componentização para garantir que todas as categorias de reciclagem (Plástico, Eletrônicos e Árvores) tenham a mesma aparência e comportamento. Isso reduz a carga cognitiva, pois o usuário aprende a interagir com um card e já domina os demais.

---

## 🛠️ Guia de Execução
Para rodar este projeto localmente, siga os passos abaixo via terminal:

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/seu-usuario/una-blazor-lista12.git](https://github.com/seu-usuario/una-blazor-lista12.git)
   ```
2. **Navegue até a pasta do projeto:**
   ```bash
   cd EcoMonitor
   ```
3. **Execute a aplicação utilizando o perfil HTTPS:**
   ```bash
   dotnet run --launch-profile https
   ```
4. **Acesse no navegador:** Geralmente disponível em `https://localhost:7xxx` (verifique a porta exibida no seu terminal).

---

## 💻 Explicação Técnica: Componentização e Parâmetros
O coração desta aplicação é o componente `EcoStatus.razor`. Para torná-lo reutilizável, utilizamos o atributo `[Parameter]` do Blazor:

* **Reutilização:** O `[Parameter]` permitiu definir propriedades como `Titulo` e `Peso` de fora do componente.
* **Flexibilidade:** Graças a isso, pudemos instanciar o mesmo componente três vezes na página `Home.razor`, atribuindo pesos diferentes para cada tipo de ação (1 para plástico, 5 para eletrônicos e 10 para árvores) sem duplicar código lógico.
* **Estado Dinâmico:** Cada instância do componente mantém seu próprio estado interno para o contador, garantindo que os pontos de uma categoria não interfiram nas outras.

## 🏆 Desafio Extra Implementado
* **Barra de Progresso:** Adicionada uma representação visual que preenche conforme os pontos aumentam.
* **Mensagem de Conquista:** Ao atingir a marca de 100 pontos, o sistema exibe a mensagem especial: *"Meta batida! Você é um Herói do Planeta!"*.
```
