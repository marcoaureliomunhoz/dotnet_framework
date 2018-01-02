## .NET Framework

> Framework é um conjunto de componentes/elementos prontos para um contexto, porém permite adaptação. Portanto é algo pronto que também é adaptável.

O .NET Framework é um conjunto de componentes/elementos prontos que simplificam o desenvolvimento e a execução de aplicações.

**Como funciona:**  
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

**Evolução:**

Ano | Versão | CLR 
--- | --- | --- 
2002 | .NET Framework 1.0 | CLR 1.0 
2003 | .NET Framework 1.1 | CLR 1.1 
2005 | .NET Framework 2.0 | CLR 2.0 
2006 | .NET Framework 3.0 | CLR 2.0 
2008 | .NET Framework 3.5 | CLR 2.0 
2010 | .NET Framework 4.0 | CLR 4.0 
2012 | .NET Framework 4.5 | CLR 4.0 
2013 | .NET Framework 4.5.1 | CLR 4.0 
2014 | .NET Framework 4.5.2 | CLR 4.0 
2015 | .NET Framework 4.6 | CLR 4.0 
2015 | .NET Framework 4.6.1 | CLR 4.0 
2016 | .NET Framework 4.6.2 | CLR 4.0  
2017 | .NET Framework 4.7 | CLR 4.0  
2017 | .NET Framework 4.7.1 | CLR 4.0  

**.NET Full Framework e .NET Core:** 

A partir de 2014 a Microsoft começou a trabalhar em uma nova geração do framework, o .NET Core (um subset do superset/full framework), que além de ser multiplataforma é mais leve (< 15MB) e customizável. A partir do .NET Core o .NET Framework, comum até a versão 4.7.1, é chamado de .NET Full Framework.

- Novos componentes da plataforma:
    - **RyuJIT**: novo JIT.
    - **Roslyn**: novo compilador.
    - **SIMD**: single instruction and multiple data (paralização em nível de CPU/núcleo).
    - **.NET Standard**: novo padrão de definição de bibliotecas para permitir reaproveitamento de código entre plataformas .NET.

**.NET Standard:**

O .NET Standard é uma especificação formal de APIs do .NET que devem estar disponíveis em todas as implementações do .NET. A motivação por trás do .NET Standard é estabelecer maior uniformidade no ecossistema do .NET. A ECMA 335 continua a estabelecer a uniformidade de comportamento da implementação do .NET, mas não há especificação semelhante para as BCLs (Bibliotecas de Classe Base) para implementações da biblioteca do .NET.

.NET Standard | 1.0 | 1.1 | 1.2 | 1.3 | 1.4 | 1.5 | 1.6 | 2.0  
--- | --- | --- | --- | --- | --- | --- | --- | ---  
.NET Core | 1.0 | 1.0 | 1.0 | 1.0 | 1.0 | 1.0 | 1.0 | 2.0  
.NET Framework | 4.5 | 4.5 | 4.5.1 | 4.6 | 4.6.1 | 4.6.1 | 4.6.1 | 4.6.1  
Mono | 4.6 | 4.6 | 4.6 | 4.6 | 4.6 | 4.6 | 4.6 | 5.4   
Xamarin.iOS | 10.0 | 10.0 | 10.0 | 10.0 | 10.0 | 10.0 | 10.0 | 10.14  
Xamarin.Mac | 3.0 | 3.0 | 3.0 | 3.0 | 3.0 | 3.0 | 3.0 | 3.8  
Xamarin.Android | 7.0 | 7.0 | 7.0 | 7.0 | 7.0 | 7.0 | 7.0 | 8.0  
Universal Windows Platform | 10.0 | 10.0 | 10.0 | 10.0 | 10.0 | 10.0.16299 | 10.0.16299 | 10.0.16299  
Windows | 8.0 | 8.0 | 8.1  
Windows Phone | 8.1 | 8.1 | 8.1  
Windows Phone Silverlight | 8.0  

**Referências:**  
- https://github.com/dotnet
- https://docs.microsoft.com/pt-br/dotnet/
- https://docs.microsoft.com/en-us/dotnet/framework/migration-guide/versions-and-dependencies
- https://en.wikipedia.org/wiki/.NET_Framework#.NET_Core
- https://github.com/dotnet/standard/blob/master/docs/versions.md
- https://docs.microsoft.com/pt-br/dotnet/standard/net-standard
