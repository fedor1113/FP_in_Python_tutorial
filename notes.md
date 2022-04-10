Алонзо Чёрч предложил 𝜆-исчисление в 1930-ых годах, хотя изначально предложенная им версия включала и логику, которая была противоречива (как было показано Клини и Россером). Тем не менее, само исчисление крайне важно для развития функционального программирования. Любой чисто функциональный язык — суть 𝜆-исчисление (сводим к нему).
Затем Алан Тьюринг совершенно независимо показал, что это исчисление полное по Тьюрингу (Turing, A. M. (1937). "Computability and λ-definability". The Journal of Symbolic Logic. Cambridge University Press. 2 (4): 153–163. doi:10.2307/2268280).


Русский математик Моисей Эльевич Шейнфинкель разработал похожую систему вообще без связанных переменных, называемую *комбина́торной логикой* и ввёл *каррирование*. Это идеи, которые из его одной работы потом разовьёт Хаскелл Брукс Карри (хотя каррирование идея, конечно, не новая и описана ещё у Фреге, например). Х. Карри в принципе выведет все необходимые принципы для последующего создания языков ФП.
Большое значение также имеет последующая разработка Чёрчем просто типизированного лямбда-исчисления (𝜆→)


*LISP* был создан создателем термина ИИ и основателем области его изучения Джоном Маккарти в 1950х (первые две имплементации написаны Стивом Расселлом). Common Lisp — обманка в некотором смысле.
Джон Бэкус, руководитель команды создателей первого высокоуровневого языка программирования Фортран, — частично наш отец, но для него и просто функциональное программирование в стандартном понимании недостаточно чистое.
Язык ML был важной вехой. Сильное функциональное программирование в Coq/Gallina (интерактивное программное средство доказательства теорем/его язык), где завершение программы за конечное время доказуемо.


```python
def cut_iterable(iterable: Iterable[Any], size: int) -> Iterable[Any]:
    """Return a new iterator from a given iterable
    that cuts it off of size size.
    """

    # return itertools.islice(iterator, 0, size)

    for cnt, item in enumerate(iterable):
        if cnt + 1 == size:
            break

        yield item
```


Python doc:


"Once tee() has made a split, the original iterable should not be used anywhere else; otherwise, the iterable could get advanced without the tee objects being informed.


tee iterators are not threadsafe. A RuntimeError may be raised when using simultaneously iterators returned by the same tee() call, even if the original iterable is threadsafe.


This itertool may require significant auxiliary storage (depending on how much temporary data needs to be stored). In general, if one iterator uses most or all of the data before another iterator starts, it is faster to use list() instead of tee()."
