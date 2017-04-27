---
title: "Prostředky aplikace Operations"
description: "Provozní prostředek provádí aktivity projektu nebo výrobního procesu. Mohou být různého typu a mohou mít různé schopnosti."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f77fe37933854d66c35a4a14e6dfb6db398eb034
ms.lasthandoff: 03/31/2017


---

# <a name="operations-resources"></a>Prostředky aplikace Operations

[!include[banner](../includes/banner.md)]


Provozní prostředek provádí aktivity projektu nebo výrobního procesu. Mohou být různého typu a mohou mít různé schopnosti. 

<a name="operations-resources"></a>Prostředky aplikace Operations
--------------------

Provozní prostředky jsou stroje, nástroje, pracovníci, zařízení, fyzické oblasti nebo dodavatelé provádějící aktivity projektu nebo výrobního procesu. Mohou být různého typu a mohou mít různé schopnosti.

-   **Dodavatel**: Externí prostředek provádějící aktivity projektu nebo výrobní operace. Jedná se například o subdodavatele. Propojením prostředků dodavatele s účtem dodavatele lze generovat nákupy pro subdodavatele na základě řádků kusovníku nebo výroby.
-   **Lidské zdroje**: Projektový nebo výrobní pracovník provádějící aktivitu samostatně nebo jako operátor nástroje nebo stroje. Pokud používáte funkci modulu Lidské zdroje, můžete propojit lidské zdroje s pracovníkem. Modul plánování může potom alokovat prostředky na základě kompetencí definovaných pro daného pracovníka.
-   **Stroj**: Stroje nebo jiné výrobní zařízení, které je nutné ve výrobě.
-   **Nástroj**: Nástroj nebo zařízení, které se obvykle používá v kombinaci s jiným prostředkem k provádění aktivit v projektu nebo výrobě.
-   **Umístění**: Fyzické umístění určité velikosti, které je vyžadováno k provedení aktivity. Může se například jednat o montážní plochu.
-   **Zařízení**: Budova nebo pevná struktura, kterou je vyžadována k provedení aktivity.

## <a name="calendars"></a>Kalendáře
Kalendář lze přiřadit k provoznímu prostředku a popisuje kapacitu prostředku (v hodinách). Pracovní doba provozního prostředku je určena kalendářem, který je přiřazen ke skupině prostředků, jejíž součástí je daný provozní prostředek. Můžete nastavit datum začátku platnosti a datum vypršení platnosti pro přiřazený kalendář. Poté můžete přiřadit více než jeden kalendář k provoznímu prostředku. Avšak data přiřazených kalendářů se nesmí překrývat a provozní prostředek může být přiřazen pouze k jednomu kalendáři v rámci jedné operace. **Poznámka:** Pokud nejsou pro skupinu prostředků v platnosti žádné pracovní kalendáře, například pokud platnost posledního přiřazeného kalendáře nebo jediného přiřazeného kalendáře vypršela, přístup k provozním prostředkům přiřazeným ke skupině prostředků není pro plánování výroby a plánování operací možný. Také můžete přiřadit kalendář ke skupině prostředků a určit pracovní doby pro skupinu prostředků a všechny provozní prostředky přiřazené k dané skupině prostředků. Kapacita skupiny prostředků se vypočítá jako součet kapacity jednotlivých provozních prostředků přiřazených k této skupině prostředků. Kalendář přiřazený ke skupině prostředků je možné měnit.

## <a name="resource-capabilities"></a>Schopnosti prostředku
Schopnost je možnost provozních prostředků provádět určitou aktivitu. Můžete přiřadit více než jednu schopnost k provoznímu prostředku. Plánovací modul potom přidělí prostředky spárováním provozních prostředků jednotlivých aktivit s možnostmi dostupných provozních prostředků. Schopnosti lze přiřadit ke všem typům provozních prostředků (**nástroj**, **dodavatel**, **stroj**, **lidské zdroje**, **umístění** nebo **zařízení**). Chcete-li přiřadit schopnosti k provozním prostředkům po omezenou dobu, určete počáteční datum a datum vypršení platnosti při přiřazování schopnosti. Další informace naleznete v části [Schopnosti prostředku](resource-capabilities.md).

## <a name="resource-groups"></a>Skupiny prostředků
Skupina prostředků je sada provozních prostředků, která představuje rozlišovací možnosti, pomocí kterých chcete plánovat prostředky, když používáte metodu plánování operací. Proto skupiny prostředků obvykle odpovídají fyzickému uspořádání pracovních buněk vyznačených žlutými pruhy ve výrobní hale. Skupina prostředků definuje pracoviště, výrobní jednotku a kontext skladu pro provozní prostředky přiřazené ke skupině. Když přiřadíte provozní prostředek ke skupině prostředků, prostředek může být naplánován na pracovišti, kde je umístěna daná skupina prostředků. Nemusíte přiřadit provozní prostředky, které vytvoříte, ke skupině prostředků. Avšak provozní prostředek musí být nejprve přiřazen ke skupině prostředků, aby bylo možné jej naplánovat k provedení práce. Provozní prostředek lze přiřadit ke skupině prostředků po omezenou dobu. Lze také přiřadit provozní prostředek k více skupinám prostředků, abyste potom mohli prostředky sdílet mezi různými pracovišti. Avšak data platnosti a data vypršení platnosti se nesmí překrývat. Jinak řečeno, nelze přiřadit provozní prostředek ke dvěma skupinám prostředků současně. Změny v přiřazení skupiny prostředků jsou platné pouze pro nová přidělení prostředků. Rezervace kapacity pro prognózy hodin úloh, operací a projektu, které jsou již naplánovány, nebudou ovlivněny. **Poznámka:** Při přiřazení provozních prostředků typu **dodavatele** ke skupině prostředků musí být všechny provozní prostředky, které jsou přiřazeny k této skupině prostředků, typu **dodavatel** a musí být propojené se stejným účtem dodavatele.

## <a name="production-units"></a>Výrobní jednotky
Výrobní jednotka je správní jednotka, která je tvořena několika skupinami prostředků. Výrobní jednotka může obsahovat více skupin prostředků, ale skupinu prostředků lze přiřadit pouze jedné výrobní jednotce. Výrobní jednotka reflektuje fyzické rozvržení výrobních zdrojů a nemá dopad na transakce a jejich zpracování. Produkční jednotku musíte přiřadit k pracovišti. Výrobní jednotce je možné také přiřadit výdejní a úložný sklad. Výrobní jednotku lze použít ke konsolidaci a filtrování dat souvisejících s výrobou. Například manažer dílenského řízení může pro konkrétní výrobní jednotku zobrazit přehled pracovního zatížení a dostupné kapacity. Výrobní jednotku přiřazenou ke skupině skupině prostředků je možné změnit. Dále je možné výrobní jednotku odstranit. Tyto změny výrobní jednotky jsou však použity pouze pro nové objednávky vytvořené po spuštění hlavního plánování. Chcete-li použít změnu výrobní jednotky na existující objednávky, je nutné tak učinit ručně.

## <a name="resource-scheduling"></a>Plánování prostředků
Provozní prostředky jsou přiřazeny k aktivitám, když je naplánován projekt nebo výroba. Jsou k dispozici dvě metody plánování: plánování operací a plánování úloh. Pokud používáte plánování operací, každá operace nebo aktivita projektu je naplánována ve skupině prostředků, která obsahuje provozní prostředky splňující požadavky prostředku, které jsou zadány pro danou operaci. Pokud operace vyžaduje určité provozní prostředky, plánování rezervuje kapacitu pouze pro specifický provozní prostředek ve skupině. Plánování úloh je podrobnější forma plánování než plánování operací. Každou operaci rozdělí na jednotlivé úkoly nebo úlohy. Tyto úkoly jsou následně přiřazeny k zdrojům operace, které je budou provádět. Plánování rezervuje kapacitu pro skupiny prostředků podle provozní doby definované ve výrobní aktivitách postupu nebo projektu. Pokud pracujete s omezenou kapacitou, plán závisí na dostupnosti provozních prostředků, které jsou zapotřebí k dokončení aktivity. V rámci plánování operací je kapacita skupiny prostředků součtem dostupné kapacity provozních prostředků, které jsou zahrnuty v dané skupině. Rezervace kapacity, které již existují pro provozní prostředky, jsou považovány za nedostupnou kapacitu. Není-li k dispozici dostatek kapacity pro výrobu, výrobní zakázky se mohou zpozdit nebo i zastavit. Na stránce **Prostředky** lze definovat několik vlastností, které řídí způsob provádění rezervací kapacity:

-   **Kapacita**: Zadejte kapacitu provozního prostředku na hodinu za použití měrné jednotky kapacity.
-   **Kapacita dávky**: Zadejte maximální počet kusů, které může zpracovat provozní prostředek za operaci.
-   **Procento účinnosti**: Určete účinnost, kterou očekáváte od provozního prostředku. Procenta účinnosti upraví propustnosti provozních prostředků a má vliv na dobu rezervovanou pro prostředek. Jsou také náležitě upraveny doby realizace pro operace, které používají provozní prostředek. Zde je vzorec použitý k výpočtu: Plánovaný čas = Čas × 100 ÷ procento účinnosti v tomto vzorci, *čas* zahrnuje operační čas a dobu nastavení.
-   **Procento plánování operací**: Zadejte maximální procento kapacity provozního prostředku, kterou chcete použít při plánování operací. Tato procentuální hodnota by měla být menší než 100 procent, aby byla při plánování úloh prací k dispozici určitá kapacitní flexibilita.
-   **Omezená kapacita**: Nastavte možnost **Ano** v případě, že provozní prostředek má být naplánován podle skutečné dostupné kapacity a zda by se měly zvážit existující rezervace kapacity. Je-li tato možnost je nastavena na hodnotu **Ne**, u provozního prostředku se předpokládá, že je nastavena neomezená kapacita, a zdroj může být tím pádem přeplněn.
-   **Omezená vlastnost**: Nastavte tuto možnost na hodnotu **Ano**, chcete-li provozní prostředek naplánovat na základě skutečné kapacity dostupné s ohledem na požadované vlastnosti plánování pracovní doby.
-   **Výhradní**: Nastavte tuto možnost na hodnotu **Ano**, pokud nechcete, aby provozní prostředek je k dispozici pro jinou práci nebo operaci až do dokončení aktuální výroby. V tomto případě nebude možné využít tento provozní prostředek ani v případě, že se v operačním čase prostředku vyskytnou volná místa.
-   **Kritický prostředek**: Definuje provozní prostředek jako kritický prostředek. Kritický zdroj je plánován s použitím omezené kapacity při výběru polí **Omezená kapacita** a **Kritické plánování** na stránce **Hlavní plány**.

Chcete-li plánovat více provozních prostředků zároveň, například k provádění operace ve výrobě, je nutné zadat požadavky na různé prostředky za použití primárních a sekundárních operací. Poté můžete také rezervovat více provozních prostředků, které mají různé kapacity. Provozní prostředky, které jsou naplánovány pro primární operace, určují dobu trvání aktivity.

## <a name="lean-work-cells"></a>Štíhlé pracovní buňky
Můžete určit, že skupina prostředků je štíhlou pracovní buňkou. Skupina prostředků může být pak součástí výrobního toku. Zadáním skupiny prostředků jako štíhlé pracovní buňky také zabráníte alokování skupiny prostředků a přiřazených provozních prostředků pro operace výrobní zakázky nebo hodinovou prognózu projektu. Pro každou skupinu prostředků, která funguje jako štíhlá pracovní buňka, je nutné určit následující informace:

-   **Kalendář**: Pracovní kalendář pracovní buňky, který musí mít vlastnost „standardní pracovní den“.
-   **Vstupní sklad a umístění**: Výchozí umístění, které se používá k výdeji materiálu pro aktivitu.
-   **Výstupní sklad a umístění**: Výchozí umístění, kde je umístěn veškerý výstup pracovní buňky.
-   **Nákladová kategorie runtime**: Tuto kategorii je nutno definovat pro pracovní buňku, pokud je v nákladech sledována přímá práce.

Při použití skupiny prostředků jako štíhlé pracovní buňky je kapacita pracovní buňky určena přímo pro skupinu prostředků. Proto nemusíte přiřadit provozní prostředky k dané skupině prostředků. Provozní prostředek typu **dodavatele** musí být přiřazen k pracovní buňce, pouze pokud je pracovní buňka spravována subdodavatelem. Pokud přiřadíte provozní prostředek ke skupině prostředků, která je označena jako pracovní buňka, kapacita pracovní buňky nebude ovlivněna.

## <a name="costing-resources"></a>Prostředky výpočtu nákladů
Při definování činnosti, například operace postupu nebo hodinové prognózy projektu, můžete zadat požadavek pro konkrétní provozní prostředek nebo skupinu prostředků. Můžete však také určit požadavek pro provozní prostředek určitého typu nebo provozní prostředek, který má specifickou schopnost nebo kompetenci. Z tohoto důvodu není provedeno vlastní přiřazení prostředku, dokud nebude naplánovaná aktivita a rezervována kapacita. Proto můžete pro operaci postupu zadat, že odhad a výpočet kusovníku musí být založeny na určitém provozním prostředku. Tento provozní prostředek je označován jako prostředek výpočtu nákladů. Můžete také přenést nákladové kategorie a časy operací z prostředku výpočtu nákladů do aktivity. Při plánování operace se odhad a výpočet kusovníku provede pomocí provozního prostředku, který je skutečně naplánován.




