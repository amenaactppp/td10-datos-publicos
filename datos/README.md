# Fuente sintética de la semana 8

`registros.json` contiene una lista que el docente hace crecer de 2 a 3, 10, 20, 50 y 100 registros. Cada objeto tiene `codigo`, `fecha`, `sede`, `hospital`, `paciente_id`, `grupo_edad`, `diagnostico`, `canal`, `estado` y una lista `medicamentos` de longitud variable. El docente también puede agregar, editar o quitar registros durante la sesión.

Los códigos de paciente son ficticios. `REG-001` y `REG-003` comparten `PAC-001`, de modo que tres registros representan dos pacientes distintos en esa etapa. El panel cuenta atenciones por hospital y diagnóstico; los medicamentos mencionados no indican tratamiento del diagnóstico.

`equivalencias.json` contiene un diccionario de variante → nombre común. Sus claves y valores se guardan con `strip().casefold()`. Así, `PARACETAMOL` y `paracetamol` se consultan igual; las diferencias de acentos y los sinónimos se unen solo con una regla explícita.

Ambos archivos se publican juntos desde el panel docente. El estudiantado los lee por la API pública de GitHub. Los datos son ficticios y se ofrecen bajo CC0 1.0; no describen pacientes, recetas, tratamientos ni inventario reales.
