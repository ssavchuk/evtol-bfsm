MAVLink
=======

MAVLink or Micro Air Vehicle Link is a protocol for communicating with small unmanned vehicle. It is designed as a header-only message marshaling library.

Для обмена данными многие современные дроны, собираемые энтузиастами, коммерческие или даже промышленные, используют протокол MAVLink.
Протокол описывает информационное взаимодействие между системами, такими как MAV и GCS(Ground control station) — станция наземного управления, а так же их составными частями — компонентами.

MAVLink – это протокол для организации связи между автономными летательными и транспортными системами (дронами, самолетами, автомобилями).

Протокол MAVLink может быть использован поверх следующих каналов связи:

* последовательное соединение (UART, USB и др.);
* UDP (Wi-Fi, Ethernet, 3G, LTE);
* TCP (Wi-Fi, Ethernet, 3G, LTE).

MAVLink-сообщение это отдельная "порция" данных, передаваемая между устройствами. Отдельное MAVLink-сообщение содержит информацию о состоянии дрона (или другого устройства) или команду для дрона.

Примеры MAVLink-сообщений:

ATTITUDE, ATTITUDE_QUATERNION – ориентация квадрокоптера в пространстве;
LOCAL_POSITION_NED – локальная позиция квадрокоптера;
GLOBAL_POSITION_INT – глобальная позиция квадрокоптера (широта/долгота/высота);
COMMAND_LONG – команда для квадрокоптера (взлететь, сесть, переключить режим и т. д.)

Полный список MAVLink-сообщений можно посмотреть в документации [MAVLink](https://mavlink.io/en/messages/common.html).

Система, компонент системы

Каждое устройство (дрон, базовая станция и т. д.) имеет ID в сети MAVLink. В PX4 MAVLink ID меняется с помощью параметра MAV_SYS_ID. Каждое MAVLink сообщение содержит поле с ID системы-отправителя. Кроме того, некоторые сообщения (например, COMMAND_LONG) содержат также ID системы-получателя.
Помимо ID систем, сообщения могут содержать ID компонента-отправителя и компонента-получателя. Примеры компонентов системы: полетный контроллер, внешняя камера, управляющий бортовой компьютер (Raspberry Pi в случае Клевера) и т. д.
