# Coso CI Godot

* Nepo nepo@mastodon
* Fernando taletronic@mastodon
(¡háblanos!)

---

# Casos de uso

* Día a día generar build de test
* Últimos 10 minutos de jam
* Generar build cuando el programador está de vacaciones/enfermo
* Evitar olvidarte de un paso concreto/instalar todo
* "En mi ordenador funciona"™️

---

# CI (Integración Continua)

* Es la traca matraca
* Build y publicar con cada cambio
* Automático
* Es código: no miente ni se olvida pasos

<span style="font-size: 30px;">Recurso para Github y Gitlab: https://github.com/abarichello/godot-ci</span>

---

# Github Actions

* Porque Microsoft lo da gratis, pero hay otros
* workflow.yml: fichero de configuración
    * Define los pasos para hacer build
    * En forma de comandos de terminal

---

# workflow.yml

* Descarga proyecto e img Docker
* Descarga datos + caché
* Versionado
* Setup export templates
* Build
* Deploy
* Notificación en discord 👍/👎 

<img 
    style="width: 20%; position: fixed; top:40%; right: 0%;" 
    src="https://s3.amazonaws.com/static.slid.es/logo/v2/slides-symbol-512x512.png" 
    />

--

![Sample image](https://s3.amazonaws.com/static.slid.es/logo/v2/slides-symbol-512x512.png)

---

# Ejemplo

* Github Actions
* Selecciona workflow
* Lanzar (hacer rama para <br/>q se vea q pasa cuando falla / <br/>hacer como sorpresa)

<img 
style="width: 20%; position: fixed; top:20%; right: 0%;" 
src="https://s3.amazonaws.com/static.slid.es/logo/v2/slides-symbol-512x512.png" 
/> 
