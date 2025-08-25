Definiciones operativas y fórmulas clave:

**1) GANs (Generative Adversarial Networks)**

* Juego min–max entre generador $G_\theta(z)$ y discriminador $D_\phi(x)$.
* Objetivo clásico:

$$
\min_{\theta}\max_{\phi}\;\; 
\mathbb{E}_{x\sim p_\text{data}}\!\big[\log D_\phi(x)\big]
+\mathbb{E}_{z\sim p(z)}\!\big[\log(1-D_\phi(G_\theta(z)))\big].
$$

* Intuición: el adversario fuerza realismo local; produce muestras nítidas.
* Riesgos: inestabilidad, *mode collapse*.
* Variantes: WGAN con distancia de Wasserstein y *gradient penalty* para estabilidad.

**2) VAEs (Variational Autoencoders)**

* Modelo latente probabilístico con *encoder* $q_\phi(z\mid x)$ y *decoder* $p_\theta(x\mid z)$.
* Se maximiza la ELBO:

$$
\mathcal{L}=\mathbb{E}_{q_\phi(z\mid x)}[\log p_\theta(x\mid z)]
-\mathrm{KL}\!\left(q_\phi(z\mid x)\,\|\,p(z)\right),
\quad z=\mu_\phi(x)+\sigma_\phi(x)\odot\varepsilon.
$$

* Intuición: espacio latente continuo y regularizado → interpolación y edición semántica.
* Riesgos: *blurriness* por likelihood gaussiano y regularización fuerte.

**3) Transformers**

* Arquitectura autoregresiva con autoatención. Factorización:

$$
p(x_{1:T})=\prod_{t=1}^{T}p(x_t\mid x_{<t});\quad 
h=\mathrm{Attn}(Q,K,V).
$$

* Genera secuencias largas con coherencia y composición simbólica.
* Condicionamiento cruzado para *image captioning*, código, música, etc.
* No es un “tipo de generador” per se sino la máquina que implementa el modelo generativo.

**4) Modelos de difusión**

* Proceso directo añade ruido: $q(x_t\mid x_{t-1})=\mathcal N(\sqrt{1-\beta_t}x_{t-1},\beta_t I)$.
* Aprenden la reversa prediciendo ruido $\varepsilon_\theta(x_t,t)$ y optimizan

$$
\min_\theta \;\mathbb{E}_{t,x,\varepsilon}\left\|\varepsilon-\varepsilon_\theta(x_t,t)\right\|^2.
$$

* Vista continua: *score matching* y SDE/ODE de denoising.
* Ventaja: alta fidelidad y control fino por *guidance* (p. ej. *classifier-free*).
* Costo: muestreo iterativo lento, aunque acelerable con solvers de pocas etapas.

**Cuándo usar qué**

* Nítidez extrema y datos abundantes de imágenes → **GANs**.
* Latentes estructurados, interpolación y compresión probabilística → **VAEs**.
* Lenguaje, código, multi-tarea secuencial, condicionamiento flexible → **Transformers**.
* Calidad SOTA, edición guiada por texto y robustez a modos → **Difusión**.

**Creatividad operacional**

* **Novedad** $\approx$ explorar regiones del soporte latente no vistas pero plausibles.
* **Valor** $\approx$ alineación con *prompts* o condicionantes.
* Mapa rápido: VAEs proporcionan continuidad del espacio ($\partial x/\partial z$ suave), GANs empujan al borde del soporte de datos, Transformers componen símbolos y relaciones largas, Difusión permite control programático del trayecto de muestreo.
Definiciones operativas y fórmulas clave:

**1) GANs (Generative Adversarial Networks)**

* Juego min–max entre generador $G_\theta(z)$ y discriminador $D_\phi(x)$.
* Objetivo clásico:

$$
\min_{\theta}\max_{\phi}\;\; 
\mathbb{E}_{x\sim p_\text{data}}\!\big[\log D_\phi(x)\big]
+\mathbb{E}_{z\sim p(z)}\!\big[\log(1-D_\phi(G_\theta(z)))\big].
$$

* Intuición: el adversario fuerza realismo local; produce muestras nítidas.
* Riesgos: inestabilidad, *mode collapse*.
* Variantes: WGAN con distancia de Wasserstein y *gradient penalty* para estabilidad.

**2) VAEs (Variational Autoencoders)**

* Modelo latente probabilístico con *encoder* $q_\phi(z\mid x)$ y *decoder* $p_\theta(x\mid z)$.
* Se maximiza la ELBO:

$$
\mathcal{L}=\mathbb{E}_{q_\phi(z\mid x)}[\log p_\theta(x\mid z)]
-\mathrm{KL}\!\left(q_\phi(z\mid x)\,\|\,p(z)\right),
\quad z=\mu_\phi(x)+\sigma_\phi(x)\odot\varepsilon.
$$

* Intuición: espacio latente continuo y regularizado → interpolación y edición semántica.
* Riesgos: *blurriness* por likelihood gaussiano y regularización fuerte.

**3) Transformers**

* Arquitectura autoregresiva con autoatención. Factorización:

$$
p(x_{1:T})=\prod_{t=1}^{T}p(x_t\mid x_{<t});\quad 
h=\mathrm{Attn}(Q,K,V).
$$

* Genera secuencias largas con coherencia y composición simbólica.
* Condicionamiento cruzado para *image captioning*, código, música, etc.
* No es un “tipo de generador” per se sino la máquina que implementa el modelo generativo.

**4) Modelos de difusión**

* Proceso directo añade ruido: $q(x_t\mid x_{t-1})=\mathcal N(\sqrt{1-\beta_t}x_{t-1},\beta_t I)$.
* Aprenden la reversa prediciendo ruido $\varepsilon_\theta(x_t,t)$ y optimizan

$$
\min_\theta \;\mathbb{E}_{t,x,\varepsilon}\left\|\varepsilon-\varepsilon_\theta(x_t,t)\right\|^2.
$$

* Vista continua: *score matching* y SDE/ODE de denoising.
* Ventaja: alta fidelidad y control fino por *guidance* (p. ej. *classifier-free*).
* Costo: muestreo iterativo lento, aunque acelerable con solvers de pocas etapas.

**Cuándo usar qué**

* Nítidez extrema y datos abundantes de imágenes → **GANs**.
* Latentes estructurados, interpolación y compresión probabilística → **VAEs**.
* Lenguaje, código, multi-tarea secuencial, condicionamiento flexible → **Transformers**.
* Calidad SOTA, edición guiada por texto y robustez a modos → **Difusión**.

**Creatividad operacional**

* **Novedad** $\approx$ explorar regiones del soporte latente no vistas pero plausibles.
* **Valor** $\approx$ alineación con *prompts* o condicionantes.
* Mapa rápido: VAEs proporcionan continuidad del espacio ($\partial x/\partial z$ suave), GANs empujan al borde del soporte de datos, Transformers componen símbolos y relaciones largas, Difusión permite control programático del trayecto de muestreo.
