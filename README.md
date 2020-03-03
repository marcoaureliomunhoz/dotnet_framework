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

**Últimas Versões do .NET Core:**

- 3.1 (LTS - Suporte a Longo Prazo)
    - Alterações significativas no Windows Forms.
    - C++/CLI.
- 3.0
    - Suporte para Windows Formas e WPF no Windows.
    - Recursos para C# 8.
    - Geração de executáveis por padrão.
    - Vinculação de assembly como medida para reduzir o tamanho final do aplicativo gerado.
    - A partir da versão 3.0 a compilação em camadas (para otimizações automáticas) vem ativada como padrão.
    - Formato ReadyToRun (R2R), que é uma forma de compilação antecipada (AOT). Os binários R2R melhoram o desempenho de inicialização reduzindo a quantidade de trabalho que o compilador just-in-time (JIT) precisa fazer à medida que seu aplicativo é carregado. Os binários contêm código nativo similar comparado ao que o JIT produziria.
    - Agora o build copia as dependências do NuGet para a pasta de saída.
    - Novas opções global.JSON.
    - Novo formato de pacote de aplicativos do Windows (MSIX).
    - Aprimoramentos para Linux.
    - Suporte de GPIO para Respberry Pi.
    - Segurança - TLS 1.3 e OpenSSL 1.1.1 no Linux.
    - Novos recursos para criptografia.
    - Novos tipos **System.Index** e **System.Range**.
    - **IAsyncEnumerable<T>** como versão assíncrona de IEnumerable<T>.
    - Atualização das APIs de ponto flutuante para entrar em conformidade com a revisão IEEE 754-2008.
    - Suporte nativo ao JSON como alternativa ao Newtonsoft.JSON.
    - Suporte a HTTP/2.
- 2.2
    - Implatanção por meio de **.exe** em vez de arquivos **.dll**.
    - Classes do tipo evento para obter informações de serivços de runtime como GC, JIT, ThreadPool e interoperabilidade.
    - Compilação em camadas será ativada mediante consentimento. A compilação em camadas serve para otimizar o código em execução. Em aplicações pequenas esses estágios de otimização podem elevar o tempo em vez de melhorar, por isso se você quiser usar a compilação em camadas precisa configurar/ativar.
    - Injeção de código antes de executar o método Main (gancho de inicialização).

**.NET Standard:**

O .NET Standard é uma especificação formal de APIs do .NET que devem estar disponíveis em todas as implementações do .NET. A motivação por trás do .NET Standard é estabelecer maior uniformidade no ecossistema do .NET. A ECMA 335 continua a estabelecer a uniformidade de comportamento da implementação do .NET, mas não há especificação semelhante para as BCLs (Bibliotecas de Classe Base) para implementações da biblioteca do .NET.

**Referências:**  
- https://docs.microsoft.com/pt-br/dotnet/core/whats-new/
- https://github.com/dotnet
- https://docs.microsoft.com/pt-br/dotnet/
- https://docs.microsoft.com/en-us/dotnet/framework/migration-guide/versions-and-dependencies
- https://en.wikipedia.org/wiki/.NET_Framework#.NET_Core
- https://github.com/dotnet/standard/blob/master/docs/versions.md
- https://docs.microsoft.com/pt-br/dotnet/standard/net-standard
