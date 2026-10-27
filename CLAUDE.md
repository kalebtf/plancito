# Plancito: instrucciones para Claude

- El dueño del proyecto habla español (México). Responde y escribe todo el texto visible para usuarios en español de México, claro y sin tecnicismos.
- Plan completo: `docs/plan.md` (resumen) y el Google Doc enlazado en el README. Respeta las reglas del juego de `docs/plan.md`; si un cambio las contradice, pregunta antes.
- Estructura: `web/` página de lista de espera (HTML estático, Netlify Forms); `app/` React Native + Expo + TypeScript (iPhone, Android y web con un solo código); `supabase/` tablas, reglas RLS y funciones; `docs/` plan y documentos.
- Diseño: look nocturno. Fondo `#15121C`, superficies `#221D2C`, texto `#F6F2EC`, acento coral `#FF5B3A`, azul `#8AD1FF`, lima `#E4F5A8`. Tipografías Bricolage Grotesque (títulos) y DM Sans (texto). Botones de al menos 44 px de alto.
- Seguridad y privacidad: nunca guardes fotos de INE ni datos de tarjeta en nuestra base de datos; viven en el proveedor de verificación y en el procesador de pagos. Toda tabla de Supabase lleva RLS activado desde su creación.
- La garantía de $250 se aparta en la tarjeta solo cuando faltan menos de 5 días para la cita (Mercado Pago cancela reservas no cobradas a los 5 días).
- Siempre se pagan experiencias, nunca personas: no agregues funciones que muevan dinero entre usuarios.
- No hagas commit ni push sin que el dueño lo pida.
