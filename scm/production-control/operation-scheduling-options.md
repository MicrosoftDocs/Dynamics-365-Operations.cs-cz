---
title: "Možnosti plánování operací"
description: "V tomto tématu jsou popsány možnosti pro plánování operací. Plánování operací můžete použít, když je třeba získat obecný odhad výrobního procesu v čase."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ede111a8c7e8fe17b95747aadef30d1af1fea6aa
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="operations-scheduling-options"></a>Možnosti plánování operací

[!include[banner](../includes/banner.md)]


V tomto tématu jsou popsány možnosti pro plánování operací. Plánování operací můžete použít, když je třeba získat obecný odhad výrobního procesu v čase.

Plán operací vypočítá následující údaje pro výrobní zakázku:

-   Počáteční a koncová data jsou nastavena pro výrobní zakázku a jednotlivé operace.
-   Operacím jsou přiřazeny prostředky.

Několik nastavení určuje způsob výpočtu plánů výroby. Tato nastavení lze definovat na stránce **Plánování operací**. Následující informace popisují možnosti plánování.

## <a name="operations-scheduling"></a>Plánování operací
### <a name="scheduling-direction"></a>Způsob plánování

Způsob plánování je základním faktorem procesu plánování. Výrobu lze naplánovat dopředu nebo zpětně od libovolného data v závislosti na požadavcích načasování a plánování.

-   **Dopředné plánování**– výrobu můžete naplánovat tak, aby se zahájila co nejdříve. Výroba může začít dnes, zítra nebo ke kterémukoli konkrétnímu budoucímu datu. Zahájení výroby je naplánováno na nejbližší možné datum a výroba je naplánována tak, aby skončila k nejbližšímu možnému datu ukončení.
-   **Zpětné plánování**– výrobu můžete naplánovat tak, aby se zahájila co nejpozději. Základem plánu je datum, kdy musí být výroba hotova, a plánuje se zpětně k nejpozdějšímu možnému datu zahájení výroby, kdy bude ještě možné dodržet termín dokončení.

Existují tyto možnosti:

-   **Vpřed ode dneška** – Plánování dopředu od aktuálního data. (Aktuální datum je systémové datum.)
-   **Vpřed od plánovaného počátku** – Plánování dopředu od dřívějšího počátečního data. Jestliže předchozí plán neexistuje, nastaví se směr plánování dopředu od aktuálního data.
-   **Vpřed od data plánování** - Plánování dopředu od data uvedeného v poli **Datum plánování**. Jestliže datum plánování nezadáte, nastaví se směr plánování dopředu od aktuálního data.
-   **Zpět od data dodání** - zpětné plánování od data dodání určeného pro výrobní zakázku. Jestliže zvolíte tuto možnost, ale nebude určeno žádné datum dodání, nastaví se datum dodání na aktuální datum.
-   **Zpět od plánovaného konce** - zpětné plánování od dříve vypočteného koncového data. Jestliže předchozí plán neexistuje, koncové datum se nastaví na aktuální datum.
-   **Zpět od data plánování** - Plánování dozadu od data uvedeného v poli **Datum plánování**. Jestliže nezadáte žádné datum plánování, použije se aktuální datum. Datum zpětného plánování ode dne akce se vypočítá pro výrobní zakázku při posledním výpočtu požadavku. Jestliže pro výrobní zakázku není určeno žádné datum, bude použito aktuální systémové datum.
-   **Zpět od data termínu** - Zpětné plánování od data termínu vypočtené pro výrobní zakázku při posledním výpočtu požadavku. Jestliže pro výrobní zakázku není určeno datum v budoucnosti, bude použito aktuální systémové datum.
-   **Dle posledního plánování** - V souvislosti s plánováním operací a rozpisy práce se ukládá vybraný způsob plánování a datum plánování. Tuto možnost lze proto zvolit pro následné plánování. Jestliže pro výrobní zakázku neexistuje předchozí plánování, bude plánování probíhat zpětně od aktuálního systémového data.
-   **Vpřed od zítřka** – Plánování vpřed od aktuálního data plus jeden den.
-   **Vpřed od předchozí úlohy** - Tato možnost má smysl jen při plánování úloh. Jestliže pro plánování operací vyberete tento způsob plánování, výrobní zakázka je naplánována vpřed od aktuálního data. Při plánování úloh se stanoví plán pro jednu úlohu a všechny další úlohy pro výrobu se naplánují podle ní.
-   **Zpět od předchozí úlohy** - Tato možnost má smysl jen při plánování úloh. Jestliže pro plánování operací vyberete tento směr plánování, plánované objednávky budou naplánovány odzadu od aktuálního data. Při plánování úloh se stanoví plán pro jednu úlohu a všechny další úlohy pro výrobu se naplánují podle ní.

### <a name="scheduling-date"></a>Datum plánování

Toto datum se používá pro směry plánování **Vpřed od data plánování** nebo **Zpět od data plánování**. Plánování potom probíhá dozadu nebo dopředu od tohoto data. Další informace o směru plánování naleznete v předchozí části Směr plánování.

### <a name="recalculate-bom-levels"></a>Přepočítat úrovně kusovníku

Když vyberete **Přepočítat úrovně kusovníku**, vybrané úrovně kusovníku budou přepočítány k zajištění správného pořadí plánování.

## <a name="limitations"></a>Omezení
### <a name="finite-capacity"></a>Omezená kapacita

Plánování závisí na dostupnosti zdrojů potřebných k dokončení výroby. Pokud není k dispozici dostatečná kapacita, mohou být výrobní zakázky odloženy nebo i zastaveny. Je-li na operace plánování aplikována konečná kapacita, berou se v úvahu existující rezervace kapacity, které se provádějí u prostředků, a tato kapacita se zobrazí jako nedostupná. Výrobní zakázka je naplánována na základě dostupnosti kapacity požadovaných zdrojů. Plánování operací používá zadané pořadí operací k určení pořadí operací ve výrobním postupu. Plánování operací rezervuje kapacitu skupin prostředků podle provozních dob definovaných ve výrobním postupu. Kapacita skupiny prostředků je součet dostupné kapacity všech prostředků ve skupinách prostředků.

### <a name="finite-material"></a>Omezený materiál

Plánování je závislé také na dostupnosti materiálů potřebných k výrobě. Nedostatečná dostupnost komponent může také způsobit zpoždění výroby. Plánování může být založeno také na použití materiálů. Stačí zadat materiály, které musí být k dispozici pro výrobu, místo materiálů, které nejsou kritické. Tento typ plánování se nazývá plánování s omezeným materiálem. Po zadání omezených materiálů bude výroba naplánovaná podle toho, zda jsou materiály k dispozici. **Poznámka:** Při optimalizaci kapacity i materiálů je výroba vypočtena tak, aby vyhovovala oběma omezením. Je zohledněna dostupnost kapacity a materiálů a zahájení operací výrobní zakázky nelze naplánovat, dokud nebude kapacita a materiály k dispozici ve stejnou dobu a v potřebných množstvích. Zaškrtnutím tohoto políčka určíte, zda se materiály při plánování mají považovat za omezené. Jsou-li materiály omezené, vezme se v úvahu pokrytí dané doby materiálem. Jinak řečeno, plánování vezme v úvahu data termínů položek, které jsou vypočtené. Plánování provede rezervaci surovin a rozpad aktuální výroby. Pokud se plánování uskuteční několikrát, k rozpadu a rezervaci dojde jen při prvním plánování. Jestliže provedete změny ve výrobním kusovníku nebo v postupu, dojde k rozpadu při dalším plánování. Pro rozpad se předpokládá, že materiály jsou potřeba v tentýž den. Protože výroba není plánována v době rozpadu hlavního plánu, jako nejlepší odhad doby, kdy budou položky k dispozici, se použije aktuální datum. Rozpad poté zkontroluje, zda jsou položky dostupné. Jestliže jsou položky dostupné, výrobní požadavek je možné splnit. Nejsou-li položky k aktuálnímu datu dostupné, vytvoří se plánovaná objednávka a pro plánovanou objednávku bude provedena vyrovnávací volba. Je-li pro plánovanou objednávku nastaveno automatické potvrzení, plánovaná objednávka bude pro nákup nebo výrobu potvrzena automaticky. Stav výroby se automaticky změní na stav uvedený v poli **Požadovaný stav výroby** v dialogovém okně **Skupiny disponibility**. Je-li zaškrtávací políčko prázdné, materiály se vždy budou považovat za dostupné. Z toho vyplývá, že plánování nebere v úvahu, zda jsou materiály dostupné v době požadavku.

### <a name="finite-property"></a>Omezené vlastnosti

Toto políčko zaškrtněte, pokud má plánování práce zahrnovat požadavky na vlastnosti.

### <a name="keep-production-unit"></a>Zachovat výrobní jednotku

Určete, zda by měl plánovací modul naplánovat pouze zdroje, které jsou již zadány ve výrobní jednotce.

### <a name="keep-warehouse-from-resource"></a>Zachovat sklad z prostředku

Určete, zda má plánovací modul naplánovat pouze zdroje, které jsou přidruženy k vstupnímu skladu, který je specifikován v prostředku.

## <a name="references"></a>Odkazy
### <a name="schedule-references"></a>Plánovat odkazy

Když reference závisejí na výrobních zakázkách, jsou známé také jako dílčí výroby. V rámci plánování výrobní zakázky lze plánovat dílčí výroby. Pokud má být plánování dílčích výrob založeno na plánování hlavní výroby, zaškrtněte toto políčko. Podle hlavní výroby se nadřízená výroba naplánuje dopředu a podřízená výroba se naplánuje zpětně. Reference výrobní zakázky lze zobrazit v poli **Referenční úroveň** na stránce **Výrobní zakázky**.

### <a name="synchronize-references"></a>Synchronizovat odkazy

Reference mohou být také synchronizovány s výrobní zakázkou. Vyberete-li tuto možnost, budou při změně plánu výrobní zakázky posunuta a vyrovnána i data dílčích výrob. Pokud výrobní zakázka obsahuje jednu nebo více dílčích výrob, můžete naplánovat dílčí výroby společně s hlavní výrobou. V takovém případě hlavní výrobu nelze zahájit až do dokončení souvisejících dílčích výrob. Proto pokud má být plánování dílčích výrob založeno na počátečním a koncovém datu vybrané výroby, zaškrtněte toto políčko. Zaškrtnete toto políčko, jen když není zaškrtnuto také políčko**Plánovat odkazy**.

## <a name="cancellation"></a>Zrušení
### <a name="cancel-queue-time"></a>Zrušit čas čekání před operací

Toto políčko zaškrtněte v případě, že chcete z plánování vyloučit dobu čekání.

### <a name="cancel-setup"></a>Zrušit nastavení

Toto políčko zaškrtněte v případě, že chcete z pánování vyloučit dobu nastavování.

### <a name="cancel-process"></a>Zrušit proces

Toto políčko zaškrtněte v případě, že chcete z pánování vyloučit dobu běhu.

### <a name="cancel-overlap"></a>Zrušit překrytí

Toto políčko zaškrtněte v případě, že chcete z pánování vyloučit dobu překrytí.

### <a name="cancel-transport"></a>Zrušit přepravu

Toto políčko zaškrtněte v případě, že chcete z pánování vyloučit dobu převodu.

## <a name="set-default"></a>Nastavit výchozí
Aktuální hodnoty můžete uložit jako výchozí hodnoty. K dispozici jsou dvě možnosti:

-   Nastavit jako moje výchozí
-   Nastavit jako výchozí pro každého


<a name="see-also"></a>Viz také
--------

[Plánování operací](operations-scheduling.md)




