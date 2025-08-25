End-to-end (E2E) = cifrado y control **desde el emisor hasta el receptor final**. Solo los extremos pueden leer los datos; **ningún intermediario** (proxys, gateways, CDNs) ve texto claro. Contraste: TLS “hop-by-hop” termina y re-abre sesiones en cada salto; E2E mantiene la carga útil opaca fuera de los extremos.

## 3) Consentimiento “granular, revocable e informado”

* **Granular:** por **scope** (p. ej., `accounts:read`, `balances:read`), cuenta, y **vigencia** (p. ej., 90 días).
* **Revocable:** el usuario lo **corta en cualquier momento**; técnicamente, revocación de tokens + cese inmediato de flujos.
* **Informado:** propósito, tercero, datos exactos, duración y riesgos, en lenguaje claro y auditable.

## 8) Embedded finance

* Ejemplo: **préstamo al checkout** en una app de e-commerce.
* Flujo: app solicita oferta → proveedor financiero evalúa vía API → aprueba y liquida en segundo plano → usuario finaliza compra **sin salir** del flujo comercial.
* Valor: menor fricción, decisión contextual y en tiempo real.

## 12) OAuth 2.0

* **Autorización delegada** basada en **tokens**. Evita compartir contraseñas con terceros.
* Patrón típico: **Authorization Code + PKCE** → token de acceso con **scopes** y expiración; opcional refresh token.
* OIDC añade **identidad** del usuario sobre OAuth.

## 14) “Platformisation”

* La entidad financiera expone **capacidades componibles** (datos, pagos, KYC) vía APIs para que **otros construyan encima**.
* Roles: **manufacturer** (productos), **aggregator** (ensambla), **distributor** (llega al usuario).
* Efecto: externalidades de red, menor costo marginal de innovación; requerir **gobernanza y responsabilidad** claras.

## 15) Tableros de consentimiento

* Clave: **gestión en tiempo real**. Revocar, acotar o pausar **con efecto inmediato** en el servidor de autorización.
* Debe mostrar: quién accede, a qué datos, con qué finalidad, desde/cuándo hasta/cuándo.
* Back-end: **token introspection**, revocación, **scopes finos** y tokens de vida corta; eventos para desactivar integraciones al instante.
