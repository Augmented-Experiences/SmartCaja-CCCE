# Skill: Estacionalidad

## Objetivo
Modelar correctamente los patrones estacionales del negocio para proyecciones más realistas.

## Patrones por Industria

### Retail / Comercio
| Mes | Factor | Razón |
|-----|--------|-------|
| Ene | 0.7 | Post-navidad, menor gasto |
| Feb | 0.7 | Vuelta a clases |
| Mar | 0.9 | Normalización |
| Abr | 0.9 | Estable |
| May | 1.0 | Día de la madre |
| Jun | 0.95 | Mitad de año |
| Jul | 0.90 | Vacaciones escolares |
| Ago | 0.95 | Estable |
| Sep | 1.05 | Amor y Amistad |
| Oct | 1.0 | Estable |
| Nov | 1.25 | Cyberlunes / HotSale |
| Dic | 1.5 | Navidad |

### Alimentos / Panadería
| Mes | Factor | Razón |
|-----|--------|-------|
| Ene | 0.85 | Post-navidad |
| Feb | 0.90 | Vuelta a clases |
| Mar | 0.95 | Normalización |
| Abr | 1.05 | Semana Santa |
| May | 1.10 | Día de la Madre |
| Jun-Jul | 0.90 | Vacaciones de mitad de año |
| Ago | 0.95 | Estable |
| Sep | 1.05 | Amor y Amistad |
| Oct | 1.0 | Estable |
| Nov | 1.10 | Temporada comercial |
| Dic | 1.25 | Navidad, panes y novenas |

### Servicios Profesionales
| Mes | Factor |
|-----|--------|
| Ene-Feb | 0.65 (vacaciones y arranque) |
| Mar-Jun | 1.1 (alta demanda) |
| Jul | 0.8 (vacaciones de mitad de año) |
| Ago-Nov | 1.1 (alta demanda) |
| Dic | 0.7 (cierre de año) |

## Fuentes de Datos
- Información directa del usuario sobre meses altos/bajos
- Búsqueda de mercado online para el sector
- Patrones históricos de la industria
- Eventos locales (Navidad, Semana Santa, Día de la Madre, Cyberlunes, etc.)

## Aplicación
El factor de estacionalidad se multiplica directamente por los ingresos base del mes:
```
Ingresos_Mes = Ingresos_Base × Factor_Estacionalidad[mes]
```
