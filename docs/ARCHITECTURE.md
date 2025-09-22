# Sudakov.Club — Архитектурные ориентиры

## Базовые технологии (MVP)
- Backend: PHP 8.4, Laravel 12.
- API: JSON API, REST.
- Realtime: WebSockets/SSE.
- Хранилище: MySQL, Redis, S3-совместимое для медиа в дальнейшем (на начальном этапе загружаемые файл храняться на локальном диске).
- Контейнеризация: Docker + docker-compose.
- Клиент: PWA (Vue/React).
- CI/CD: GitHub Actions.

## Ключевые сущности
Family, Member, Role, Permission, Profile, Post, Comment, Thread, Message, Album, Media, Event, RSVP, KnowledgeEntry, TimeCapsule, GenealogyNode, ShareLink, AuditLog.

## Приватность
- Уровни доступа: Private / Family / Extended / Link.
- Роли и политики доступа (RBAC/ABAC).
- AuditLog фиксирует шаринг, приглашения и действия.

## Децентрализация
- MVP — один приватный инстанс.
- Задел: идентификаторы сущностей, экспорт/импорт данных, совместимость с будущим протоколом.
- Центральный портал: **точка входа** для семьи и описание протокольной идеи.
