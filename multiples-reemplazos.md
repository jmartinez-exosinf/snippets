# 🧩 Definir Múltiples Reemplazos en un Snippet con Snippet Designer 2022

Este tutorial te muestra cómo definir **múltiples reemplazos** en un snippet usando **Snippet Designer 2022** en Visual Studio 2022. Los reemplazos permiten que el usuario personalice partes del código al momento de insertar el snippet.

---

## 🎯 ¿Qué es un reemplazo?

Un **reemplazo** es una variable dentro del snippet que el usuario puede modificar al insertarlo. Se define usando `$nombre$` en el código y se configura como `<Literal>` o `<Object>` en el XML.

---

## ⚙️ Pasos para definir múltiples reemplazos en Snippet Designer

1. Abre **Visual Studio 2022**.
2. Asegúrate de tener instalada la extensión **Snippet Designer 2022**.
3. Ve a `File > New > File > Code Snippet File`.
4. Escribe tu código en el editor.
5. Selecciona las partes que deseas convertir en reemplazos (por ejemplo, tipo de dato y nombre de variable).
6. Haz clic derecho sobre la selección y elige **"Make Replacement"**.
7. En el panel de propiedades, define:
   - `ID`: nombre del reemplazo (ej. `tipoDato`, `nombreVariable`)
   - `ToolTip`: descripción breve
   - `Default`: valor por defecto
8. Repite el proceso para cada reemplazo que desees agregar.
9. Guarda el archivo `.snippet`.

---

## 🧪 Ejemplo práctico

### Código con reemplazos:
```csharp
$tipoDato$ $nombreVariable$ = default($tipoDato$);
```

### Fragmento XML generado:
```xml
<CodeSnippets xmlns="http://schemas.microsoft.com/VisualStudio/2005/CodeSnippet">
  <CodeSnippet Format="1.0.0">
    <Header>
      <Title>Declaración de variable</Title>
      <Shortcut>vardecl</Shortcut>
      <Description>Declara una variable con tipo y nombre personalizados</Description>
      <Author>Jose Nestor</Author>
    </Header>
    <Snippet>
      <Declarations>
        <Literal>
          <ID>tipoDato</ID>
          <ToolTip>Tipo de dato de la variable</ToolTip>
          <Default>int</Default>
        </Literal>
        <Literal>
          <ID>nombreVariable</ID>
          <ToolTip>Nombre de la variable</ToolTip>
          <Default>miVariable</Default>
        </Literal>
      </Declarations>
      <Code Language="csharp"><![CDATA[
$tipoDato$ $nombreVariable$ = default($tipoDato$);
$end$
]]></Code>
    </Snippet>
  </CodeSnippet>
```

Este snippet permite al usuario definir el tipo de dato y el nombre de la variable al insertarlo, y posiciona el cursor justo después de la línea para continuar escribiendo.
