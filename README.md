## .NET Framework

> Framework é um conjunto de componentes/elementos prontos para um contexto, porém permite adaptação. Portanto é algo pronto que também é adaptável.

O .NET Framework é um conjunto de componentes/elementos prontos que simplificam o desenvolvimento e a execução de aplicações.

**Como que funciona:**  
 1. **Codificação**: você codifica (código fonte) em uma liguagem criada sobre MSIL.
2. **Compilação Intermediária**: processa o resultado da codificação através de um dos compiladores disponíveis. O compilador gera um **assembly intermediário** baseado em MSIL/CIL.
3. **Execução**: o CRL (ambiente de execução) processa e executa (gerencia) o resultado da compilação intermediária. Quando necessário aciona o JIT (just-in-time compiler) para gerar código de máquina ou o GC (garbage collector) para limpar a memória.

**Principais componentes:**
- **Compilador Intermediário**: processa o código fonte e gera assembly intermediário baseado em MSIL/CIL. 
    - **csc.exe**: compilador da linguagem C#.
- **CLR**: gerenciador/ambiente de execução (common language runtime).
- **JIT**: converte o código MSIL/CIL para o código de máquina correspondente à plataforma (SO) onde a aplicação é executada.
- **GC**: garbage collector (coletor de lixo).
- **NET Class Libraries**: conjunto de bibliotecas do framework.
- **ILDASM**: utilitário para ver o código MSIL/CIL.

> A conversão do código fonte para MSIL/CIL é feita de acordo com a **Common Language Specification (CLS)** e a **Common Type System (CTS)** que especificam respectivamente um conjunto de funções básicas e um conjunto de tipos básicos que todas as linguagens da plataforma devem suportar.
