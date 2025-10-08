# Regras de Desenvolvimento e Tech Stack

Este documento descreve a pilha de tecnologia utilizada no projeto "Encontro Certo" e as diretrizes para o uso de bibliotecas e frameworks.

## Tech Stack

*   **Framework:** React (com TypeScript)
*   **Roteamento:** React Router
*   **Estilização:** Tailwind CSS
*   **Componentes UI:** shadcn/ui (construído sobre Radix UI)
*   **Ícones:** Lucide React
*   **Serviços de IA:** Google Gemini API
*   **Backend (Mocked):** Supabase (para autenticação e dados)
*   **Build Tool:** Vite

## Regras de Uso de Bibliotecas

Para manter a consistência e a eficiência no desenvolvimento, siga estas regras ao utilizar as bibliotecas e frameworks:

*   **React (com TypeScript):** Utilize para construir todos os componentes da interface do usuário e gerenciar o estado da aplicação. Sempre use TypeScript para tipagem.
*   **React Router:** Empregue para todas as necessidades de roteamento no lado do cliente, definindo as rotas em `src/App.tsx`.
*   **Tailwind CSS:** **Sempre** utilize Tailwind CSS para estilização. Priorize classes utilitárias para layout, espaçamento, cores e outros aspectos de design. Evite estilos inline ou arquivos CSS personalizados, a menos que estritamente necessário para overrides específicos.
*   **shadcn/ui:** Use os componentes pré-construídos do shadcn/ui para elementos comuns da UI (botões, modais, inputs, etc.). **Não edite os arquivos dos componentes shadcn/ui diretamente.** Se precisar de uma variação ou funcionalidade extra, crie um novo componente que envolva ou estenda o componente shadcn/ui.
*   **Radix UI:** É a base para os componentes shadcn/ui. Não é esperado o uso direto de componentes Radix UI, a menos que você esteja construindo um componente complexo do zero que não tenha um equivalente no shadcn/ui.
*   **Lucide React:** Utilize para todos os ícones na aplicação.
*   **Google Gemini API:** Exclusivamente para funcionalidades de Inteligência Artificial, como moderação de conteúdo (texto e imagem), análise de compatibilidade e sugestões de mensagens.
*   **Supabase (Mocked):** Atualmente, o Supabase é mockado para simular serviços de autenticação e gerenciamento de dados. Interaja com ele através do `supabaseService.ts`.
*   **Vite:** É o bundler e servidor de desenvolvimento. As configurações são gerenciadas em `vite.config.ts`.

Ao seguir estas diretrizes, garantimos um codebase limpo, manutenível e com uma experiência de usuário consistente.