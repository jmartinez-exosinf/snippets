# 🧩 Usar `$selected$` en Snippets con Snippet Designer 2022

## 🎯 ¿Qué es `$selected$`?
`$selected$` es un marcador especial que representa el código que el usuario tiene seleccionado en el editor cuando inserta el snippet. Esto permite envolver código existente con estructuras predefinidas.

---

## ⚙️ Pasos para crear un snippet con `$selected$`

1. Abre **Visual Studio 2022** y asegúrate de tener instalada la extensión **Snippet Designer 2022**.
2. Crea un nuevo archivo de snippet:
   - `File > New > File > Code Snippet File`.
3. Escribe la estructura que deseas usar para envolver código, por ejemplo:
```csharp
try {
    $selected$
}
catch (Exception ex) {
    Console.WriteLine(ex.Message);
}
```
4. Guarda el snippet en tu carpeta de snippets:
```dir
Documents\Visual Studio 2022\Code Snippets\Visual C#\My Code Snippets\
```

Define un **Shortcut** (ej. trywrap) para activarlo fácilmente con **Ctrl+K, X**.

## 🧪 Ejemplo XML del snippet
```xml
<CodeSnippets xmlns="http://schemas.microsoft.com/VisualStudio/2005/CodeSnippet">
  <CodeSnippet Format="1.0.0">
    <Header>
      <Title>Try-Catch Wrapper</Title>
      <Shortcut>trywrap</Shortcut>
      <Description>Envuelve el código seleccionado en un bloque try-catch</Description>
      <Author>Jose Nestor</Author>
    </Header>
    <Snippet>
      <Code Language="csharp"><![CDATA[
try
{
    $selected$
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}
$end$
]]></Code>
    </Snippet>
  </CodeSnippet>
</CodeSnippets>
```

## ✅ ¿Por qué es útil?
- Te permite aplicar patrones comunes sin reescribir código.
- Ideal para agregar manejo de excepciones, logging, o validaciones alrededor de código existente.
- Ahorra tiempo y reduce errores manuales.
