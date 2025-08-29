# 🛠️ Verificar si SQL Server local está activo (Windows CMD)

Este documento resume los principales comandos para comprobar si el servidor **SQL Server** local está funcionando en Windows.  

---

## 📋 Tabla de Comandos y Usos en cmd


| Comando | ¿Para qué sirve? |
|---------|------------------|
| `sc query type= service state= all \| find "SQL"` | Lista **todos los servicios** relacionados con SQL Server instalados en el sistema. |

| `sc query MSSQLSERVER` | Verifica el **estado del servicio principal** de SQL Server (instancia por defecto). |

| `sc query MSSQL$MiInstancia` | Comprueba el estado de una **instancia con nombre**. |

| `net start \| find "SQL"` | Muestra qué **servicios SQL están iniciados** actualmente. |

| `telnet localhost 1433` | Testea si SQL Server está **escuchando en el puerto 1433** (por defecto). |

| `ping localhost` | Verifica que el equipo responda, útil como primer chequeo de conectividad. |

| `netstat -ano \| find "1433"` | Comprueba si hay un proceso **escuchando en el puerto 1433**. |

| `sqlcmd -S localhost -U sa -P TuPassword` | Intenta una **conexión directa al motor SQL** usando el cliente de línea de comandos. |


