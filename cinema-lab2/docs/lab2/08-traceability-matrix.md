# 8. Обновлённая матрица трассируемости

| ID требования | Бизнес-цель | Use Case | Класс / метод | Таблица БД | Тест-кейс |
|---------------|-------------|----------|---------------|-----------|-----------|
| FR-01 | Показать репертуар | UC-01 | FilmService.listFilms() | movie | TC-01: список фильмов |
| FR-02 | Дать сведения о фильме | UC-01 | FilmService.getDetails() | movie | TC-02: детали фильма |
| FR-03 | Помочь выбрать время | UC-02 | ScreeningService.listByFilm() | screening | TC-03: расписание по фильму |
| FR-04 | Показать параметры сеанса | UC-02 | ScreeningService.getDetails() | screening, hall | TC-04: время, зал, цена |
| FR-05 | Показать доступность мест | UC-03 | TicketService.getSeatMap() | seat, ticket | TC-05: занятые места |
| FR-06 | Выбрать место | UC-04 | TicketService.checkAvailability() | seat, ticket | TC-06: свободное место |
| FR-07 | Оформить продажу | UC-05 | TicketService.sellTicket() | ticket | TC-07: билет создаётся |
| FR-08 | Исключить двойную продажу | UC-05 | TicketService.sellTicket() | ticket | TC-08: второй билет отклонён |
| FR-09 | Хранить историю продажи | UC-05 | TicketRepository.save() | ticket | TC-09: запись сохранена |
| FR-10 | Разрешить допустимую отмену | UC-06 | TicketService.cancelTicket() | ticket | TC-10: отмена до сеанса |
| FR-11 | Добавлять фильмы | UC-07 | FilmService.createFilm() | movie | TC-11: создание фильма |
| FR-12 | Обновлять каталог | UC-07 | FilmService.updateFilm() | movie | TC-12: изменение фильма |
| FR-13 | Управлять залами | UC-08 | HallService.saveHall() | hall, seat | TC-13: сохранение зала |
| FR-14 | Создавать расписание | UC-09 | ScreeningService.createScreening() | screening | TC-14: создание сеанса |
| FR-15 | Не допускать конфликты | UC-09 | ScreeningService.checkTimeConflict() | screening | TC-15: пересечение отклонено |
| FR-16 | Считать QR | UC-10 | TicketValidationService.validateQrCode() | ticket | TC-16: токен считывается |
| FR-17 | Проверить билет и сеанс | UC-10 | TicketValidationService.validateScreening() | ticket, screening | TC-17: билет другого сеанса |
| FR-18 | Показать данные билета | UC-10 | TicketService.getTicketInfo() | ticket, screening, hall, seat | TC-18: дата, зал, место |
| FR-19 | Определить статус | UC-11 | Ticket.validate() | ticket | TC-19: отменённый билет |
| FR-20 | Исключить повторный проход | UC-11 | Ticket.markAsUsed() | ticket | TC-20: повторное сканирование |
| FR-21 | Подтвердить проход | UC-11 | TicketValidationService.confirmEntry() | ticket, ticket_check | TC-21: билет → USED |
| FR-22 | Показать заполненность | UC-12 | OccupancyService.getOccupancy() | ticket, screening, seat | TC-22: число занятых мест |
| FR-23 | Обновлять заполненность | UC-13 | OccupancyService.refresh() | ticket | TC-23: после прохода |
| FR-24 | Показать свободные места | UC-12 | TicketService.getSeatMap() | seat, ticket | TC-24: занятые/свободные |