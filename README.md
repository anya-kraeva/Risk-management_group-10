# Risk-management_group-10
Dataset 10, group 161, Participants Kraeva Anna, Semenova Ekaterina, Musinov Danila, Alexandrov Stepan

## (Marat) 24/03/2020 (repository as of 23/03/2020)

### CAR-(ROC-) curves

It's computationally correct. Disagree that rating has PIT philosophy. Note that PIT rating is suppose to change with economic cycle and incorporate impact of current conditions on borrower's credit risk.

Current grade: 1 point.

### PDs

It's computationally correct.

Current garde: 2 points

### Quality tests

1. Pls, indicate the method you use to evaluate CI for PDs.

2. LR test for PD model specifications is applied incorrectly. First, note that you are insert log-likelihood values into the  formula and it contradicts the nature of that formula. Second, the degrees of freedom in formula of critical value is supposed to be different. Pls, fix it.

3. A proportion test should to be carried out for different categories. For example, I2 and I3. The idea is to find out if  default proportions in different categories indicate different probability of defaults in these categories. 

Current grade: 1 point. Resolve the problems to get other 2 points.

### TPM

It's computationally correct.

**Problems**

1. Indicate which matrices are the final result of the calculation on spreadsheet 4.1, as there are no notations and it seems like you two matrices for each data samples.  

2. Please, explain observed differences in matrices by different methods. 

3. There are no estimates for 5-year matrices by duration method. Make sure that you calculate TPMs (transition probability matrices) out of them correctly. The idea is to model the default occurrence process for each year separately, estimate TPM of each year, infer 5-year TPM as their multiplication and (if you want) compare the result with model that assumes no difference in default intensities over all year (purely homogeneous model). Please, also note that you should apply the entire ME (Matrix Exponential) formula to all individual generators. For example, in order to estimate TPM over 01.07.2012-01.07.2013 you should run summation in ME formula over all k (till convergence) using 
<img src="https://render.githubusercontent.com/render/math?math=t=1">
and generator estimated on 01.07.2012-01.07.2013 data. For estimation 5-year TPM in a purely homogeneous model, you should run summation in ME formula over all k (till convergence) using 
<img src="https://render.githubusercontent.com/render/math?math=t=5">
 and generator estimated on 01.07.2012-01.07.2017 data.

For self-check use ME calculators, for example, like [this](https://comnuan.com/cmnn01015/) allowing copying generator matrix right from Excel spreadsheet. 

Current grade: 1 point. Resolve the problems to get other 2 points.

### Portfolio losses

Can not see what is done and what the result looks like.

Current grade: 0. 

---------------------------------

Current total project score: 5 points (potentiality 9).

---------------

## (Marat) 27/03/2020 (repository as of 27/03/2020)

*Буду писать по-русски для экономии времени*

**Stocks**

Все хорошо. Вот только ряд вопросов. Уж коль стали делать бэктеcт для 10дневного VaR, хотя никто не просил. Вот вы провели бэктест для 10дневного VaR. Во-первых, с какими доходностями Вы сравниваете 10дневный VaR для определения пробоя и как эти доходности посчитаны. Во-вторых, сколько наблюдений в периоде бэктестирования? В-третьих, все ли предположения для биномиального теста (одинаковая вероятность пробоя и их независимость) соблюдаются в вашем тесте?

Текущий балл: 4 (-1 за бэктест, поскольку понимание концепта не продемонстрировано)

**Текущий итого по рыночным риска: 4**

**Кредит_риски_v2.xlsx**

*CAP(ROC)*
С диагнозом рейтинговой философии не согласен. См. комментарий в телеге.

Текущий балл: 1

**PDs**

Все ок.

Текущий балл: 2

**Quality test**

Вэри вандерфул! Только порядок вычитания путаете в LR тесте. Из LLF усеченной модели нужно вычитать LLF неусеченной модели. Статистика будет положительной.

Ну и все-таки нужно проделать вычисления для всех лет, тогда будет еще балл.

Текущий балл: 2 

**TPM**

1. Пятилетние матрицы, когортный метод!!! За такое обещал расстреливать без суда и следствия. Обратите внимание, что сумма по строкам не равна 1. Вспомните, как получить двухлетную МПВ, имея однолетние МПВ за каждый из двух лет? Исправить!

2. После исправлений нужно прокомментировать различия оценок матриц, полученных по разным методам.

Текущий балл: 0 (Исправите будет 3)

**Portfolio**

1. Откуда взяли PD PIT и TTC? 

2. Указано, что реализованы биномиальная модель и Васичека? Я вижу только одну. Она задумывалась как модель Васичека или биномиальная? (объясните, добавлю балл).

Текущий балл: 1 

**Текущий итог по кредитным рискам: 6**