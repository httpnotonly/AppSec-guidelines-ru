
# Рекомендации по использованию сериализации

1. Не использовать сериализацию вообще  
2. Если п.1 невыполним, то использовать сериализатор, который удовлетворяет ВСЕМ условиям:

* Не хранит информацию о типах в сериализованном объекте
* Не поддерживает magic-методы в процессе десериализации
* Осуществляет строгий контроль ожидаемых и десериализуемых типов по всему дереву сериализованного объекта, начиная с корня  
    (т.е. в котором нет неявных приведений типов, в т.ч. по иерархии наследования),  
    в идеале — требующий явного указания схемы сериализуемого объекта.