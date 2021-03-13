---
title: Ukazatele KPI majetku
description: V tomto tématu jsou vysvětleny ukazatelé KPI v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectKPI
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f75db96926e72bab80d0a65ce6f0ab3a92590699
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021773"
---
# <a name="asset-kpis"></a>Ukazatele KPI majetku

[!include [banner](../../includes/banner.md)]

 

V modulu Správa majetku můžete vypočítat různé klíčové ukazatele výkonnosti (KPI) pro majetek a typy majetku. KPI se používají k získání přehledu výkonnosti pro majetek například ve vztahu k provozuschopnosti, prostoje, času opravy a průměrné době mezi závadami.

1. Klikněte na **Správa majetku** > **Dotazy** > **Majetek** > **Ukazatele KPI majetku**.

2. V dialogovém okně **Vypočítat KPI majetku** zvolte **Časové měřítko**, které bude použito ve výpočtu, a období v polích **Od data** a **Do data**. 

3. Na záložce s náhledem **Záznamy k zahrnutí** můžete v případě potřeby vybrat konkrétní majetek a typy majetku, které mají být zahrnuty do výpočtu.

4. Výpočet zahájíte klepnutím na tlačítko **OK**.

5. Na záložce s náhledem **Přehled** jsou výsledky výpočtu zobrazeny v zobrazení mřížky. Každý majetek se zobrazí na samostatném řádku.

6. Na záložce s náhledem **KPI pro vybraný řádek** jsou zobrazeny výpočty pro majetek vybraný na záložce s náhledem **Přehled**. Hodnoty KPI jsou rozděleny do kategorií **Čas** **Dostupnost**, **Pracovní příkazy**, **Údržba**, **Závady**, **Prostoj údržby** a **Náklady**.

V následující tabulce naleznete popis polí na stránce **KPI majetku**.

| Pole                   | Popis                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Majetek                   | ID majetku                                                                                                                                                                                                                                                                                             |
| Celkový čas              | Celkový čas nastavený v kalendáři použitém ve výpočtu. Pokud je majetek spojený se zdrojem, použije se související kalendář zdroje. Pokud majetek nesouvisí se zdrojem, použije se kalendář vybraný v poli **Standardní kalendář** v **Parametrech správy majetku**. |
| Doba od spuštění                  | Celkový čas mínus prostoj.                                                                                                                                                                                                                                                                            |
| Odstávka                | Registrace prostojů údržby provedené u majetku ve vybraném období.                                                                                                                                                                                                                              |
| Čas opravy             | Celkový počet pracovních hodin spotřebovaných na pracovní příkazy opravy.                                                                                                                                                                                                                                            |
| Dostupnost v %          | Provozuschopnost rozdělená celkovým časem a vynásobená 100.                                                                                                                                                                                                                                                   |
| Počet závad        | Počet příčin závad registrovaných u příznaků závad na majetku ve vybraném období.                                                                                                                                                                                                             |
| MTBF                    | Průměrná doba mezi selháním, což je celkový čas dělený počtem závad registrovaných na majetku ve vybraném období. Pokud je počet závad roven nule, průměrná doba mezi selháním je nastavena na celkový čas.                                                                                                                   |
| Míra selhání               | 1 děleno průměrnou dobou mezi selháním.                                                                                                                                                                                                                                                                                    |
| Střední doba opravy                     | Průměrná doba opravy, což je čas opravy dělený počtem závad registrovaných na majetku ve vybraném období. Pokud je počet závad roven nule, průměrná doba opravy je nastavena na čas opravy.                                                                                                                           |
| Počet přerušení         | Počet registrací prostoje údržby vytvořených na majetku.                                                                                                                                                                                                                                     |
| MTBS                    | Průměrná doba mezi zastaveními, což je celkový čas dělený počtem registrací prostoje údržby. Pokud je počet registrací prostoje údržby nula ve vybraném období, hodnota průměrné doby mezi zastaveními je nastavena na celkový čas.                                                                                      |
| Preventivní náklady         | Náklady zaúčtované na majetek související s typem nákladů "preventivní" ve vybraném období. Typy nákladů se nastavují v typech pracovních příkazů.                                                                                                                                                                       |
| Opravné náklady         | Náklady zaúčtované na majetek související s typem nákladů "Opravné" ve vybraném období. Typy nákladů se nastavují v typech pracovních příkazů.                                                                                                                                                                       |
| Hodnota náhrady       | Hodnota definovaná na majetku jako reprodukční náklady.                                                                                                                                                                                                                                                  |
| Typ majetku             | Identifikace typu majetku vybraného v majetku.                                                                                                                                                                                                                                             |
| Výrobce           | Identifikace výrobce vybraného v majetku.                                                                                                                                                                                                                                                 |
| Model                   | Identifikace modelu výrobce vybraného v majetku.                                                                                                                                                                                                                                           |
| Od data               | Počáteční datum výpočtu KPI. Pokud byl majetek vytvořen po počátečním datu vybraném pro výpočet, zobrazí se v tomto poli počáteční datum majetku.                                                                                                                                  |
| Do data                 | Koncové datum výpočtu KPI. Pokud byl majetek registrován jako neaktivní před tím, než bylo vybráno koncové datum pro výpočet, bude v tomto poli zobrazeno datum, od kterého již byl majetek neaktivní.                                                                                               |
| Časové měřítko              | Během výpočtu ukazatelů KPI vyberte časové měřítko, které bude použito: hodiny, dny nebo týdny.                                                                                                                                                                                                            |
| Dostupnost            | Provozuschopnost dělená celkovým časem.                                                                                                                                                                                                                                                                         |
| Pracovní příkazy             | Celkový počet pracovních příkazů zahrnutých ve výpočtu KPI.                                                                                                                                                                                                                                          |
| Čas pracovního příkazu         | Celkový počet pracovních hodin spotřebovaných na pracovní příkazy.                                                                                                                                                                                                                                               |
| Primární pracovní příkazy     | Počet primárních pracovních příkazů zahrnutých ve výpočtu KPI.                                                                                                                                                                                                                                        |
| Sekundární pracovní příkazy   | Počet sekundárních pracovních příkazů zahrnutých ve výpočtu KPI.                                                                                                                                                                                                                                      |
| Pracovní příkazy údržby | Počet pracovních příkazů údržby zahrnutých ve výpočtu KPI. Pracovní příkaz údržby je pracovní příkaz, který nemá související příčiny závad.                                                                                                                                                             |
| Čas údržby        | Celkový počet pracovních hodin spotřebovaných na pracovní příkazy údržby.                                                                                                                                                                                                                                       |
| Opravné pracovní příkazy      | Počet pracovních příkazů opravy zahrnutých ve výpočtu KPI. Pracovní příkaz opravy je pracovní příkaz, který má související příčinu závady.                                                                                                                                                                        |
| Spolehlivost v %           | Výpočet založený na očekávaném exponenciálním vývoji registrací závad majetku, což znamená, že v čase je majetek méně spolehlivý kvůli opotřebení. Výpočet KPI je založen na průměrné době mezi selháními a celkovém čase.                                                            |
| MTPS                    | Průměrná doba zastavení výroby, což je prostoj údržby dělený počtem registrací prostoje údržby. Pokud je počet registrací prostoje údržby nula ve vybraném období, hodnota průměrné doby mezi zastaveními je nastavena na nulu.                                                                               |
| Celkové náklady              | Celkové náklady zaúčtované na majetek ve vybraném období.                                                                                                                                                                                                                                              |
| Investiční náklady         | Náklady zaúčtované na majetek související s typem nákladů "Investice" ve vybraném období. Typy nákladů se nastavují v typech pracovních příkazů.                                                                                                                                                                       |

Na následujícím obrázku je uveden snímek obrazovky výpočtu KUV pro čtyři majetky.

![Snímek obrazovky výpočtu KUV pro čtyři aktiva](media/11-controlling-and-reporting.png)

- V části **Všechen majetek** můžete vícenásobně vybrat několik kusů majetku a kliknout na tlačítko **KPI majetku** na kartě **Obecné**. Pak klikněte na **OK** v dialogovém okně **Vypočítat KPI majetku** pro výpočet KPI u vybraného majetku.  
- Výsledky výpočtu KPI mohou, ale nemusí zahrnovat [registrace prostojů údržby](../work-orders/maintenance-downtime.md), v závislosti na nastavení a použití kódů důvodu prostoje údržby. 

