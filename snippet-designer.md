# 🧩 Snippet Designer en Visual Studio 2022

## ¿Qué es Snippet Designer?

**Snippet Designer 2022** es una extensión gratuita para Visual Studio que permite crear y editar fragmentos de código (`.snippet`) de forma visual. Algunas de sus características:

- Editor visual para crear snippets.
- Soporte para C#, VB.NET, HTML, XML, SQL, etc.
- Inserción de reemplazos (`$variable$`) fácilmente.
- Explorador de snippets.
- Exportación rápida desde el editor de código.

🔗 [Descargar desde Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=vs-publisher-2795.SnippetDesigner2022)

---

## ⚙️ Cómo instalar y usar Snippet Designer

### 1. Instalación

- Abre Visual Studio 2022.
- Ve a `Extensions > Manage Extensions`.
- Busca **Snippet Designer 2022** y haz clic en **Download**.
- Reinicia Visual Studio para completar la instalación.

### 2. Crear un nuevo snippet

- Ve a `File > New > File > Code Snippet File`.
- Escribe tu código y usa clic derecho para agregar **reemplazos**.
- Guarda el archivo `.snippet` en:
```dir
Documents\Visual Studio 2022\Code Snippets\Visual C#\My Code Snippets\
```
- Usa **Ctrl + K**, **X** para insertar snippets en el editor de código.

## 🧪 Ejemplo de snippet básico (.snippet XML)
```xml
<?xml version="1.0" encoding="utf-8"?>
<CodeSnippets>
    <Snippet>
      <Code Language="CSharp">
        <![CDATA[
Console.WriteLine("$mensaje$");
        ]]>
      </Code>
      <Declarations>
        <Literal>
          <ID>mensaje</ID>
          <ToolTip>Texto a mostrar</ToolTip>
          <DefaultText>Hola mundo</DefaultText>
        </Literal>
      </Declarations>
    </Snippet>
  unitarias, acceso a base de datos, o logging.
```
