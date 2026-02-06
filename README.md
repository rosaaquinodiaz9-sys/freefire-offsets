# Offsets Free Fire

Repositorio con offsets extraídos de la librería `libil2cpp.so` de **Free Fire** (versión 1.120.1), para uso en proyectos de desarrollo y personalización.


## 📋 CARACTERÍSTICAS
- Offsets organizados para funciones clave del juego.
- Archivos listos para usar en mods o herramientas de análisis.
- Actualizado al 06/02/2026.


## 📂 ARCHIVOS INCLUIDOS
| Archivo                  | Descripción                                  |
|--------------------------|----------------------------------------------|
| `offsets_encontrados.txt` | Lista completa de resultados brutos del análisis. |
| `offsets_freefire.json`   | Offsets organizados en formato JSON estructurado. |


## 🎯 OFFSETS PRINCIPALES
| Función                  | Offset Hexadecimal |
|--------------------------|--------------------|
| `UnityEngine.AIModule`   | `0x097c9948`       |
| `AimAssist`              | `0x097dc478`       |
| `SkillGroupBullet`       | `0x097dd3e9`       |
| `ShootingTargetConfig`   | `0x097dadf4`       |


## 🛠️ CÓMO SE EXTRAJERON
Los offsets se obtuvieron usando **Radare2** en Termux, con el siguiente comando:
```bash
radare2 -qc "e bin.relocs.apply=true; aa; izz | grep -i 'aim\|target\|bullet\|radar'" libil2cpp.so > offsets_encontrados.txt
