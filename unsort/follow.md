# follow  
Модуль предназначен для реализации функций следования за целью в системах автономного управления. Этот модуль позволяет транспортному средству определять положение и движение объекта, за которым оно должно следовать.

- **get_target_heading_deg()** : number | nil  
Возвращает текущий курс цели в градусах. Если цель не определена, возвращает `nil`.


- **get_target_location_and_velocity_ofs()** : ( Location | nil ) & ( Vector3f | nil )  
Получает текущее местоположение цели и её скорость **с учетом заданных смещений.** Функция возвращает два значения: объект `Location_ud`, представляющий местоположение цели, и объект `Vector3f_ud`, представляющий скорость цели в формате вектора. Если информация о цели недоступна, функция возвращает `nil` для обоих значений.


- **get_target_location_and_velocity()** : (Location | nil) & (Vector3f | nil)  
Предоставляет текущее местоположение и скорость цели **без учета смещений.** Аналогично предыдущей функции, возвращает объект `Location_ud` для местоположения и объект `Vector3f_ud` для скорости. Если цель не доступна, оба значения будут `nil`.


- **get_last_update_ms()** : uint3  
Возвращает время в миллисекундах с момента последнего успешного обновления данных о цели. Это позволяет оценить актуальность данных.


- **have_target()** : boolean  
Проверяет, есть ли в настоящий момент активная цель для отслеживания. Возвращает `true`, если цель присутствует, и `false` в противном случае.
