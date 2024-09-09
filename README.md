# CURSO: APRENDE BLAZOR

# LECCIÓN 31: Servicio NavigationManager (Parte 2)

1. Abrir la aplicación con Visual Studio 2022 o VSCode

2. A través del servicio NavigationManager también podemos obtener el valor actual de la ruta y la ruta base del componente actual:

```razor
@page "/"

<PageTitle>Home</PageTitle>

@inject NavigationManager Navigation

<p>Current URL: @currentUrl</p>

<p>Base URI: @baseUri</p>

@code {
    string? currentUrl;
    string? baseUri;

    protected override void OnInitialized()
    {
        // Get the current URL
        currentUrl = Navigation.Uri;
        baseUri = Navigation.BaseUri;
    }
}
```
