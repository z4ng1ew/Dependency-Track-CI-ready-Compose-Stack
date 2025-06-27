```markdown
# SecureCodeFuzzTrack  
**Автоматизированный анализ безопасности и фаззинг для Java-проектов**  

## Основные технологии  
- **Docker Compose**: Запуск Dependency-Track и PostgreSQL.  
- **Jazzer**: Фаззинг Java-функций для поиска уязвимостей.  
- **CycloneDX**: Генерация SBOM для анализа зависимостей .  
- **Dependency-Track**: Мониторинг уязвимостей через NVD.  

## Установка  
```bash  
docker-compose up -d  
mvn test  # Для запуска фаззинга  
```  

## Интеграция  
- BOM-файл (`target/bom.xml`) загружается в Dependency-Track для анализа.  
- CI/CD (GitHub Actions): Автоматическая проверка зависимостей и тестирование.  

## Дополнительно  
- Настройки PostgreSQL: `POSTGRES_INITDB_ARGS` для оптимизации.  
- Health-checks для стабильности контейнеров.  
```  
