# Plancito

**Él te invita a un plan real. Tú eliges.**

Plancito es una app de citas donde el hombre propone un plan concreto (qué, dónde y cuándo), deja una garantía de que va a llegar, y la mujer elige con quién salir. Todos se verifican con video e INE y las citas son siempre en lugares públicos.

Plan completo del proyecto: [Plancito: plan del proyecto (Google Docs)](https://docs.google.com/document/d/1Bo2kO4SE1RMpbias5tCxDdv0qabJS4oZV0FErmX74Iw/edit). Resumen en [`docs/plan.md`](docs/plan.md).

## Estado

| Parte | Estado |
| --- | --- |
| Página de lista de espera (`web/`) | Lista para publicar en Netlify |
| App para iPhone, Android y web (`app/`) | Por empezar (fase 2) |
| Base de datos y servidor (`supabase/`) | Por empezar (fase 2) |

## Estructura

```
plancito/
├── web/          Página de lista de espera (HTML estático + Netlify Forms)
├── app/          App con React Native + Expo (iPhone, Android y web)
├── supabase/     Tablas, reglas de seguridad y funciones del servidor
├── docs/         Plan, decisiones y documentos legales
└── netlify.toml  Configuración para publicar web/
```

## Página de lista de espera

Es HTML estático, sin dependencias. Para verla en tu computadora, abre `web/index.html` en el navegador.

Para publicarla:

1. En [Netlify](https://app.netlify.com), crea un sitio nuevo desde este repositorio (Add new site › Import an existing project › GitHub › `plancito`).
2. Netlify lee `netlify.toml` y publica la carpeta `web/`.
3. En el sitio, ve a **Forms** y activa la detección de formularios. Los registros llegan al formulario `lista-espera`.
4. Antes de recibir registros reales, completa los datos entre corchetes del aviso de privacidad (`web/aviso-de-privacidad.html`) y revísalo con un abogado.

Para medir de dónde llega la gente, usa links con `?utm_source=` o `?ref=` (por ejemplo `?utm_source=instagram&utm_campaign=prueba1`). El valor se guarda en el campo `origen` de cada registro.

## Tecnología (fase 2)

- **App:** React Native con Expo y TypeScript, un solo código para iPhone, Android y web.
- **Base de datos, cuentas y chat:** Supabase.
- **Verificación de identidad:** Didit (alternativas: Truora, MetaMap).
- **Garantía:** Mercado Pago o Stripe con cobro diferido.
- **Mapas y check-in:** Google Maps.
