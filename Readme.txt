- Импортироать данные do ##class(NPMLBI.UkraineMap).populateRegions()
- Сгенерировать тестовые данные do ##class(NPMLBI.TestData).populateTestData()
- Перенести иконки маркеров в /csp/broker/images
- В виджете "Карта"  указать (если не сделать, то маркеры будут стандартными)  (сейчас там прописаны ссылки на хостинг с картинками)
	Marker Special Icon = /csp/broker/images/mapMarkerPink.png
	Marker Icon = /csp/broker/images/mapMarkerAzure.png
	
	
Изменения в портлете
Добавлены опции:
Marker Special Icon - адрес икоки для специального маркера 
Marker Special Property - имя свойства из выборки для установления спец иконки (0/1). Пример - областные центры выделены спец маркером, а остальные города - обычным
если Marker Special Icon = "", то маркер будет выглядеть как в Marker Icon, а если и Marker Icon="", то все маркеры стандартные от гугл. 

Additional Info - информация во всплывающей подсказке над полигоном/маркером в скобках
Additional Info Property - имя свойства из выборки для установления значения доп.инфы
Структура: [имя полигона/маркера] ([Additional Info Property] [Additional Info])
Пример: Киев (12334 тыс.чел.), где Additional Info Property = TotalValue,а Additional Info = тыс.чел

если Additional Info="", то выводится просто имя полигона в подсказке