Резервные копии (РК) - копии проектов, предназначенные для восстановления работоспособности ССА и/или для модификации проектов и последующей загрузки в ССА.
РК подготавливаются для учета и хранения:
- каждая единица РК (для каждой технически обособленной единицы ССА) должна быть представлена либо одним файлом (например, РК формата zwt для контроллеров ControlWave), либо должна быть помещена в однофайловый архив (например, РК формата mwt для контроллеров ControlWave).
- в названии файлов РК должно сохраняться нативное имя, в соответствии с обозначением в ССА (если применимо) или в соответствии с диспетчерским наименованием
- название файла РК не должно включать модификаторы, не имеющие практического смысла (например, имя автора, дописки "последняя версия", "самая последняя версия" и т.п.)


РК должна быть идентифицируемая по следующим признакам:
1. Наименование объекта, ССА и обособленной единицы в составе ССА для которой подготовлена РК
2. Дата, время создания РК
3. Исполнитель, выполнявший резервное копирование
4. Причина создания РК: периодическое плановое резервное копирование, перед/после внесений изменений
5. Объем изменений и автор изменений, если РК создавалась после внесения изменений
6. Использованное ПО для создания РК
7. РК не верифицирована или верифицирована: проверкой работоспособности на оборудовании, пробной сборкой проекта или проверкой целостности образа (например, CloneZilla integrity check)
8. Контрольная сумма или иные уникальные идентификаторы, изменяющиеся при внесении изменений в проект. Если средствами разработки ПО для работы с проектами или средствами разворачивания РК (CloneZilla, КиберБэкап и т.п.) невозможно идентифицировать РК, то подготовка РК включает расчет контрольной суммы для идентификации РК (md5-сумма по файлу РК).
9. Акутальность: актуальна или не актуальна, вносились изменения

Хранение РК обеспечивается на сетевых дисках.
Доступ к РК обеспечивается по ссылкам из АСМО.
Размещение, удаление РК на сетевом диске выполняется лицом, определенное ответственным за содержание архива РК.


****
fSSAObjectId
	"Объект"
	Целое
fBackupDateTime
	"Дата/время копирования"
	Дата/время
fBackupProducer
	"Исполнитель"
	Строка (не справочник, т.к. может быть третье лицо, не учтенное в АСМО)
fBackupReason
	"Причина копирования"
	Справочник
fBackupEdits
	"Объем изменений"
	Строка UNICODE
fBackupSoftware
	"ПО для копирования"
	Справочник
fBackupVerified
	"Верификация"
	Справочник
fBackupCRC
	"Контрольная сумма"
	Строка
fBackupActual
	"Актуальность"
	Справочник
fBackupPath
	"Адрес хранения"
	Строка