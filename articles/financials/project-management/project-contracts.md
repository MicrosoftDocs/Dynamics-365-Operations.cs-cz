---
title: "Projektové smlouvy"
description: "Toto téma popisuje projektové smlouvy (obsahuje i příklady), které můžete vytvořit pro různé typy projektů a zdroje financování, dále způsoby, jak lze spravovat smlouvy a fakturovat odběratele projektu v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3a1bfd4bd5f396c05277159ac112eaa8197d5818
ms.openlocfilehash: c8328bd2d93bbe763e629248edc1b7b4576005ae
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="project-contracts"></a>Projektové smlouvy

[!include[banner](../includes/banner.md)]


Tento článek popisuje projektové smlouvy (obsahuje i příklady), které můžete vytvořit pro různé typy projektů a zdroje financování, dále způsoby, jak lze spravovat smlouvy a fakturovat odběratele projektu v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

Typ projektu, který vytvoříte pro smlouvu projektu, určuje metodu použitou při fakturaci odběratelům projektu. Můžete změnit projektovou smlouvu a související projekt, ale nelze změnit typ projektu. 

Pomocí projektové smlouvy můžete fakturovat jeden nebo několik projektů současně. Smlouva projektu rovněž pomáhá zajistit, aby byl pro každý dílčí projekt v projektové struktuře použit stejný fakturační postup. 

Každý projekt, který bude fakturován, musí být přidružen k projektové smlouvě. Nastavení projektové smlouvy platí pro všechny projekty a dílčí projekty, které jsou přidruženy k dané projektové smlouvě. 

Projektová smlouva může určit jeden nebo více zdrojů financování. Díky tomu je možné rozdělit účtování mezi více investorů, nastavit limity financování, aby zdrojům financování nebyla účtována větší než určená částka, a nakonfigurovat pravidla financování pro účtování výdajů.

## <a name="funding-for-project-contracts"></a>Financování pro smlouvy projektu
Některé projektové smlouvy uvádí, že více stran sdílí odpovědnost za financování nákladů na projekt. Několik příkladů:

-   Velký odběratel, která má několik divizí, požaduje, aby bylo financování projektu rozděleno dle divizí.
-   Vaše společnost sdílí náklady na velký projekt s externí organizací.
-   Projekt cesty je financován společně dvěma obcemi.
-   Projekt mostu je financován státním grantem a soukromou společností.

V aplikaci Finance and Operations můžete rozdělit účtování pro jednu transakci nebo celý projekt mezi více odběratelů, grantů nebo organizací. 

V projektech s více investory se všechny strany, které přispívají k financování projektu s rozšířeným financováním, nazývají zdroje financování. Po definování odběratele, organizace nebo grantu jako zdroje financování může být přiřazen k jedné nebo více pravidlům financování. Pravidla financování obsahují kritéria, která určují, jak jsou náklady přidělovány různým zdrojům financování pro projekt. 

Vzhledem k tomu, že položky na skladě, jako jsou ty, které se zobrazí v nákupním žádankách a nákupních objednávkách, nelze rozdělit, nelze rozdělit částky nákladů mezi více zdrojů financování v době distribuce. Hodnota zdroje financování tedy zůstane 0 (nula), dokud nebude zaúčtován skladový výdej. Při zaúčtování skladového výdeje bude částka nákladů rozdělena podle pravidel rozúčtování pro projekt.

Zde jsou některé kroky, které vám usnadňují rozdělení účtování mezi více zdrojů financování:

-   Určete, že všechny transakce, které jsou zadány pro projekt, používají stejnou prodejní měnu jako projektová smlouva.
-   Nastavte limity financování tak, aby zdroj financování nebyl fakturován více, než je zadaná částka projektu.
-   Konfigurujte pravidla financování a limity financování pro každého pracovníka, položku, kategorii, skupiny kategorií a typ transakce (nebo pro všechny typy transakcí).
-   Vyberte volitelná počáteční a koncová data vymezující období, kdy každé pravidlo financování platí.
-   Zadejte procentuální hodnotu, za kterou je zodpovědný každý zdroj financování.
-   Určete, jaký zdroj financování je odpovědný za zaokrouhlení rozdílů, které jsou způsobeny výpočty přidělení financování.
-   Nastavte pravidla, která určují, jak jsou náklady projektu fakturovány externím odběratelům a účtovány interním organizacím.
-   Zaznamenejte transakce na účet blokovaného financování, dokud nejsou získány další finanční prostředky nebo se nerozhodnete nést náklady interně.

Chcete-li určit daňovou skupinu a přidružit ji k transakci, projekt vyhledává přidělování daňové skupiny. Pokud nebylo provedeno přiřazení žádné daňové skupiny na úrovni projektu, bude vyhledána projektová smlouva.

### <a name="example-multiple-funding-sources-simple"></a>Příklad: Více zdrojů financování (jednoduché)

Následující tabulka obsahuje situace pro správu přidělení financování mezi více zdrojů financování. Tyto situace jsou založeny na následujících předpokladech:

-   Nastavení priority se promítnou do přiřazení prostředků před použitím jiných kritérií pravidla financování.
-   Nebyl zadán žádný rozsah dat k určení období d v případě, že pravidlo financování platí.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scénář</strong></td>
<td><strong>Zdroj financování </strong></td>
<td><strong>Přidělená procenta </strong></td>
<td><strong>Priorita přidělení </strong></td>
</tr>
<tr class="even">
<td>Chcete přidělit náklady jednomu zdroji financování do vyčerpání finančních prostředků, přidělte náklady druhému zdroji financování, dokud nebudou vyčerpány jeho finanční prostředky, a nakonec přidělte zbývající náklady třetímu zdroji financování.</td>
<td><ul>
<li>Zdroj　financování　1</li>
<li>Zdroj　financování　2</li>
<li>Zdroj　financování　3</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Chcete přidělit 75 procent nákladů jednomu zdroji financování a 25 % druhému zdroji financování. Pokud je některý z těchto zdrojů financování vyčerpán, chcete zbývající náklady uhradit ze třetího zdroje financování.</td>
<td><ul>
<li>Zdroj　financování　1</li>
<li>Zdroj　financování　2</li>
<li>Zdroj　financování　3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Chcete přidělit 75 procent nákladů jednomu zdroji financování a 25 % druhému zdroji financování. Pokud je některý z těchto zdrojů financování vyčerpán, chcete rozdělit zbývající náklady mezi třetí zdroj financování a čtvrtý zdroj financování.</td>
<td><ul>
<li>Zdroj　financování　1</li>
<li>Zdroj　financování　2</li>
<li>Zdroj　financování　3</li>
<li>Zdroj　financování　4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Chcete přidělit prvních 25 procent nákladů jednomu zdroji financování a zbytek druhému zdroji financování.</td>
<td><ul>
<li>Zdroj　financování　1</li>
<li>Zdroj　financování　2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Příklad: Více zdrojů financování (složité)

K dispozici jsou tři zdroje financování, které chcete použít v následujícím pořadí:

1.  Použijte zdroj financování 2 a zdroj financování 3 rovnoměrně, dokud nebude zdroj financování 2 vyčerpán.
2.  Pokračujte v používání zdroje financování 3, dokud jej nevyčerpáte.
3.  Použijte zdroj financování 1, až bude zdroj financování 3 vyčerpán.

Chcete-li tento cíl splnit, postupujte následovně:

-   Nastavte limity financování pro zdroj financování 2 a zdroj financování 3, odpovídající jejím částkám.
-   Vytvořte následující pravidla financování:
    -   Pravidlo 1 (Priorita 1): Přidělte 50 procent transakcí financování zdroji financování 2 a 50 procent zdroji financování 3.
    -   Pravidlo 2 (Priorita 2): Přidělte 100 procent transakcí zdroji financování 3.
    -   Pravidlo 3 (Priorita 3): Přidělte 100 procent transakcí zdroji financování 1.

Toto nastavení funguje, protože transakce jsou kontrolovány dle pravidel a limitů, aby bylo možné určit, zda některé z nich platí pro transakci. Pokud pro transakci neplatí žádné konkrétní pravidlo nebo limit, platí pravidlo Všechny transakce. Pravidlo Všechny transakce platí pro všechny transakce. 

Je-li nalezeno pravidlo, které odpovídá transakci, je nejdříve použito procento přidělené danému pravidlu, ale až po kontrole shod oproti všem limitům, které byly nastaveny. Pokud byl splněn limit a byly vyčerpány prostředky zdroje financování, pravidlo financování přidružené k limitu financování bude ignorováno a program zkontroluje následující pravidlo, které lze použít. 

V některých případech lze dle pravidla rozdělit pouze část transakce. K tomu může dojít, protože bylo dosaženo limitu při přidělení transakce. V tomto případě lze pouze určitou částku přidělit podle tohoto pravidla, jako například 50 procent, každému zdroji financování. To je případ pravidla 1, které je popsáno dříve v tomto oddílu. Zbytek bude přidělen podle dalšího pravidla v pořadí. 

Následující tabulka zkoumá tuto situaci podrobněji.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Výběr </strong></td>
<td><strong>Podrobnosti </strong></td>
</tr>
<tr class="even">
<td>Pravidla financování</td>
<td><ul>
<li>Pravidlo 1 (Priorita 1): Všechny transakce. Přidělte zdroj financování 2 ve výši 50 % a zdroj financování 3 ve výši 50 %.</li>
<li>Pravidlo 2 (Priorita 2): Všechny transakce. Přidělte zdroj financování 3 ve výši 100 %.</li>
<li>Pravidlo 3 (Priorita 2): Všechny transakce. Přidělte zdroj financování 1 ve výši 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Limity financování</td>
<td><ul>
<li>Limit zdroje financování 1 = 10 000,00</li>
<li>Limit zdroje financování 2 = 500,00</li>
<li>Limit zdroje financování 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transakce 1</td>
<td><strong>Částka transakce:</strong> 100,00<strong>Financovaní:</strong> Transakce bude zaplacena pouze podle pravidla 1, protože transakce je plně zaplacena po použití pravidla 1. Transakce je financována rovnoměrně mezi zdrojem financování 2 a zdrojem financování 3.
<ul>
<li>Zdroj financování 2: 50,00</li>
<li>Zdroj financování 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transakce 2</td>
<td><strong>Částka transakce:</strong> 5 000,00<strong>Financování:</strong> Transakce se vyplácí podle všech tří pravidel.Pravidlo 1 <strong>Pravidlo 1</strong>
<ul>
<li>Zdroj financování 2: 450,00</li>
<li>Zdroj financování 3: 450,00</li>
</ul>
<strong>Pravidlo 2</strong>
<ul>
<li>Zdroj financování 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Pravidlo 3</strong>
<ul>
<li>Zdroj financování 1: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Celkové prostředky rozdělené pro každý zdroj financování</td>
<td><ul>
<li>Zdroj financování 1: 3 850,00</li>
<li>Zdroj financování 2: 500,00</li>
<li>Zdroj financování 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Pravidla účtování
Když sjednáváte projektovou smlouvu s odběratelem, definujete, kdy a jak můžete fakturovat odběrateli za práci na projektu. Jakmile nastavíte projektovou smlouvu a projekt, můžete nastavit pravidla účtování pro projekt. Pravidla účtování jsou založena na podmínkách projektu stanovených v projektové smlouvě. Pravidla účtování, která můžete vytvořit, závisí na podmínkách v projektové smlouvě a typu projektu, jako je Čas a materiál nebo Pevná cena, který přidružíte k pravidlům účtování. Můžete vytvořit více než jedno pravidlo pro projektovou smlouvu. Lze také přiřadit pravidlo účtování více projektům, které jsou přidružené ke stejné projektové smlouvě a mají podobná platební podmínky. 

Můžete vytvářet následující typy pravidel účtování:

-   **Jednotka dodání** – Fakturujte odběratele po dokončení jednotky dodání. Jednotky dodání definujete ve smlouvě.
-   **Průběh** – Fakturujte odběratele po dokončení určitého procenta projektu. Pravidla účtování můžete nastavit pro automatické vypočítání procenta dokončené práce nebo můžete ručně vypočítat procento dokončené práce a částku k fakturaci odběrateli.
-   **Milník** – Fakturujte odběratele v plné výši milníku projektu při dosažení milníku.
-   **Poplatek** – Fakturujte odběratele za služby plus správní poplatek, což je obvykle procento nákladů služby.
-   **Čas a materiál** – Fakturujte odběratele za hodnotu času a materiálů použitých v projektu.

Pro všechny typy pravidel účtování můžete zadat procento zadržení, o které se mají snížit faktury odběratele, než projekt dosáhne dohodnuté fáze. Procento zadržení platby je určeno ve smlouvě projektu. Částka je vypočítávána na základě a odečtena od celkové hodnoty řádků na faktuře odběratele. 

Pro pravidla účtování **Čas a materiál** a **Průběh** je možné přiřadit fakturovatelné kategorie. Fakturovatelné kategorie označují transakce, které mají být zahrnuty do faktur odběratelů. 

Až budete připraveni fakturovat odběrateli, částka k fakturaci pro projekt je vypočtena na základě pravidel účtování a je vygenerován návrh projektové faktury. 

Následující části obsahují příklady, které ukazují, jak nastavit a spravovat pravidla účtování pro projekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Příklad: Vytvoření pravidla účtování na základě počtu dodaných jednotek

Vaše organizace uzavře smlouvu na poskytnutí celkem pěti školení zaměstnancům odběratele za cenu 10 000 za relaci školení. Fakturujete odběratele po každé vzdělávací relaci. 

Když nastavujete pravidla účtování pro smlouvu, použijte následující hodnoty:

-   Jednotka dodání je jedna relace školení.
-   Jednotková cena je 10 000 za relaci školení.
-   Celkový počet jednotek je pět školení.

Po dokončení jedné relace školení můžete vytvořit fakturu na 10 000 za první dodanou jednotku a odeslat fakturu odběrateli.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Příklad: Vytvoření pravidla účtování na základě udaného procenta dokončení projektu (ruční výpočet)

Vaše organizace, softwarová konzultační firma, uzavře smlouvu s odběratelem na vývoj části produktu, který odběratel vyvíjí. Vaše organizace se zaváže k doručování kódu softwaru během období šesti měsíců. Odběratel souhlasí uhradit vaší organizaci celkem 100 000 za práci. Vytvoříte pravidlo účtování pro fakturaci odběratele na základě procenta dokončené práce na projektu, jak je uvedeno ve smlouvě.

-   Na konci prvního měsíce se sejdete s odběratelem, abyste určili procento dokončené práce. Po kontrole projektu vy a odběratel usoudíte, že je projekt dokončen z 15 procent.
-   Vytvořte fakturu na 15 000 (15 procent ze 100 000) a odešlete ji odběrateli.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Příklad: Vytvoření pravidla účtování na základě udaného procenta dokončení projektu (automatický výpočet)

Vaše organizace, která se zabývá vývojem softwaru, souhlasí s vývojem balíčku pro mzdové účetnictví pro odběratele za cenu 30 000. Odběratel souhlasí uhradit vaší organizaci na základě procenta dokončené práce. Náklady na projekt odhadujete na 20 000. Projektová smlouva určuje kategorie práce, které máte použít v procesu účtování. Můžete nastavit pravidla účtování, která automaticky vypočítají částky faktur pro procentuální část práce dokončenou v každé kategorii. Nastavte rozpočet pro každou kategorii:

-   **Vývoj** – náklady 15 000 a výnos 20 000
-   **Instalace** – náklady 5 000 a výnos 10 000

Při prvním vytváření faktury odběratele je částka faktury automaticky vypočítána z následujících informací:

-   Za měsíc odešle pracovník na projektu časový rozvrh pro projekt. Náklady na hodiny pracovníka jsou 5 000 za vývoj a 1 000 za instalaci. Vývojové práce jsou z 33 procent dokončeny (5 000 skutečné náklady / 15 000 rozpočtové náklady) a instalační práce jsou dokončeny ze 20 procent (1 000 skutečné náklady / 5 000 rozpočtové náklady).
-   Částka faktury 8 667 je automaticky vypočtena (33 procent ze 20 000 + 20 procent z 10 000).
-   Vytvořte fakturu na 8 667 a odešlete ji odběrateli.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Příklad: Vytvoření pravidla účtování na základě dohodnutých milníků

Vaše organizace, poradenská firma v oblasti managementu, souhlasí s provedením průzkumu trhu pro spotřebitelský produkt, které odběratel plánuje prodávat. Zákazník souhlasí s využitím vašich služeb po dobu tří měsíců, počínaje březnem a souhlasí, že vaší organizaci zaplatí 50 000. Projekt obsahuje tři milníky:

-   Milník 1: Shromáždění spotřebitelských dat – 31. března
-   Milník 2: Analýza spotřebitelských dat – 30. dubna
-   Milník 3: Předložení zprávy o životaschopnosti produktu – 31. května

Odběratel souhlasí s platbou 10 000 vaší organizaci za první milník, 20 000 za druhý milník a 20 000 za třetí milník. 

Při nastavování projektové smlouvy souhlasíte s fakturací odběratele na základě dokončeného milníku. Pravidlo účtování zahrnuje následující kroky:

-   Definujte milníky projektu.
-   Definujte částku k fakturaci odběratele při dokončení jednotlivých milníků.

Po dokončení první milníku 31. března označte milník jako dokončený a pak vytvořte fakturu na částku 10 000 a odešlete ji odběrateli. Nelze vytvořit fakturu pro milník, dokud není označen jako dokončený.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Příklad: Vytvoření pravidla účtování na základě služeb a správního poplatku

Vaše organizace, která se zabývá poradenstvím v oblasti managementu, souhlasí s provedením průzkumu trhu za účelem vyhodnocení životnosti produktu, který odběratel (maloobchodní společnost), vyvíjí. V podmínkách smlouvy je uvedeno, že poskytnete služby tří nejlepších poradců v oblasti managementu, kteří provedou výzkum za náklady na bázi času a materiálu. Odběratel se zavazuje platit 100 za hodinu a správní poplatek ve výši 10 procent za konzultační hodiny, které jsou účtovány v projektu. 

Při nastavování projektové smlouvy vytvořte pravidlo účtování pro přidání správního poplatku 10 procent za konzultační hodiny účtované v projektu. 

Při vytváření faktury pro odběratele je odběrateli fakturován správní poplatek 10 procent a náklady na konzultační hodiny. Například pokud tři konzultanti pracovali celkem 200 hodin na projektu, bude vytvořena faktura na částku 22 000 na základě následující kalkulace:

-   200 hodin za 100 za hodinu = 20 000
-   10procentní správní poplatek = 2000
-   Celková fakturovaná částka = 22 000

Pokud poplatky zdaňuje odběratel a vy vyberete skupinu DPH v projektové smlouvě, skupina DPH je automaticky zadána do pravidel účtování pro poplatky.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Příklad: Vytvoření pravidla fakturace pro hodnotu času a materiálu

Vaše organizace, která nabízí poradenství v oblasti softwaru, se zavazuje poskytnout odběrateli pět technických poradců pro práci na projektu vývoje softwaru po dobu následujících šesti měsíců. Odběratel souhlasí s platbou 150 za každou konzultační hodinu a náklady na kancelářské potřeby. Vaše organizace odešle fakturu odběrateli na konci každého měsíce. 

Při nastavování projektové smlouvy souhlasíte s fakturací odběratele každý měsíc za čas a materiál v projektu. Vytvoříte pravidlo účtování, které obsahuje následující informace:

-   Časové období smlouvy je šest měsíců.
-   Konzultační čas se počítá ze sazby 150 za hodinu.
-   Kancelářské potřeby jsou fakturovány za náklady a celkové náklady na projekt nesmí přesáhnout 10 000.
-   Faktura odběratele se vytváří na konci každého kalendářního měsíce během projektu.

Během prvního měsíce je zaznamenáno celkem 800 hodin konzultanty na projektu. Náklady na kancelářské potřeby zaúčtované v projektu jsou 2 000. Proto na konci měsíce vytvoříte fakturu na 122 000, která se vypočítá jako 800 hodin za 150 za hodinu a 2 000 za kancelářské potřeby.




