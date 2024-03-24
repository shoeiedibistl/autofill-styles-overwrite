# input-autofill-overwrite-browser-styles

<b>supports: chrome, firefox</b>

<b>особенности работы:</b><br>
    -   <b>Решено</b> <s>заливка инпута после автозаполнения применяется не стандартная, а остается из состояния "focus" (возможно, и что-то еще кроме заливки). но ее можно назначить отдельно </s><br>
    -   <b>Больше не требуется</b> <s>можно устанавливать свою заливку для инпута при автозаполнении (свойство box-shadow inset)</s>  <br>
    -   <b>Решено</b> <s>не работает transition для box-shadow после автозаполнения, в т.ч. и для заливки фона (резкое появление) </s><br>
    -   <b>Решено</b> <s>не накладывается заливка фона при :hover, даже через js </s><br>
    -   <b>Проверить</b> автоматически может не сбрасываться состояние focus при очистке input.value скриптом, только после ручного прокликивания. теоретически может помочь дополнительная установка и снятие фокуса скриптом после такой очистки (проверить). По идее, сейчас должно сбрасываться как надо <br>
    -   хром вроде как блокирует автозаполнения пароля. в фф работает <br>
    -   в фф на инпутах для удаления желтого фильтра выставлен background:inherit, либо  при автозаполнении некоторых инпутов (телефон, пароль, возможно, какие-то еще) background будет с наложенным желтым фильтром. При использовании background:inherit поведение при наличии в инпуте фонового изображения или градиента не проверял <br>
    -   в фф на некоторых полях не возвращается стандартный плейсхолдер после очистки поля (телефон, пароль, возможно, какие-то еще). с кастомным проблем быть не должно <br>
    -   Пока неясно, как работает в совокупности с parsley или другими валидаторами, особенно с масками телефона. По идее, проблем быть не должно <br>
    -   <b>!!! протестировано в хроме и фф !!!</b> 
возможно, для других браузеров потребуется дописать скрипт и стили для фокуса, ховера, селекта и тд по аналогии с input:-webkit-autofill
