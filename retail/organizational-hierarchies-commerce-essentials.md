---
title: "Organizace a hierarchie organizace (Základy obchodování)"
description: "Základy obchodování mají tři typy vnitřní organizace, které můžete definovat na pomoc organizaci provádět obchodní proces nebo dosáhnout cíle."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 17d434f5d49d544003ee7cb862391d88ac5c723a
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Organizace a hierarchie organizace (Základy obchodování)

[!include[banner](includes/banner.md)]


Základy obchodování mají tři typy vnitřní organizace, které můžete definovat na pomoc organizaci provádět obchodní proces nebo dosáhnout cíle. 

Organizace je skupina lidí, kteří spolupracují na provádění obchodního procesu nebo dosažení cíle. Organizační hierarchie představuje vztahy mezi obchodními jednotkami, které tvoří vaši organizaci.

## <a name="organizations"></a>Organizace
V modulu Základy obchodování můžete definovat tři typy interních organizací: právnické osoby, provozní jednotky a týmy. V aplikaci Microsoft Dynamics AX jsou všechny interní organizace typy strany entity. Proto tyto organizace používají adresáře k ukládání adres a dalších kontaktních informací. Strana, což může být osoba nebo organizace, může patřit do jednoho nebo více adresářů.
### <a name="legal-entities"></a>Právnické osoby

Právnická osoba je organizace, která má registrovanou nebo uzákoněnou právní strukturu. Právnické osoby mohou uzavírat právní smlouvy a je po nich vyžadována příprava výkazů s informacemi o jejich výkonu. Společnost je v aplikaci Microsoft Dynamics AX druhem právnické osoby a každá právnická osoba je spojena s identifikátorem společnosti. Toto přiřazení existuje, protože ID společnosti nebo DataAreaId jsou použity v některých modelech dat, kde jsou společnosti použity jako hranice pro zabezpečení dat. Uživatelé mohou přistupovat k datům pouze pro společnost, ke které jsou aktuálně přihlášeni.

### <a name="operating-units"></a>Provozní jednotky

Provozní jednotka je organizace, která se používá k rozdělení řízení ekonomických zdrojů a operačních procesů v podniku. Osoby v provozní jednotce jsou povinni maximalizovat využívání omezených zdrojů, zdokonalovat procesy a zvažovat jejich výkon. V modulu Základy obchodování patří k typům provozních jednotek nákladová střediska, obchodní jednotky, hodnotové proudy, oddělení a maloobchodní kanály. V následující tabulce jsou uvedeny další informace o typech provozních jednotek.
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Typ provozní jednotky** | **Popis**                                                                         | **Účel**                                                                                                                                 |
| Obchodní jednotka           | Částečně samostatná provozní jednotka vytvořená tak, aby naplňovala strategické obchodní cíle. | Obchodní jednotky se používají pro finanční vykazování podle průmyslových odvětví nebo produktových řad, které organizace nabízí v rámci právnických osob. |
| Maloobchodní síť          | Provozní jednotka, která představuje kamenný obchod.                             | Umožňuje spravovat a řídit jeden nebo více skladů v rámci právnických osob.                                                               |

## <a name="organizational-hierarchies"></a>Organizační hierarchie
V modulu Základy obchodování je každé hierarchii přiřazena účel. Účel hierarchie určuje typy organizací, které mohou být zahrnuty v hierarchii. Účel také určuje, v jakých scénářích aplikace lze hierarchii použít. Například hierarchii maloobchodu lze používat k nákupu a prodeji výrobků v kamenném obchodě. Organizace v hierarchii mohou sdílet parametry, zásady a transakce. Organizace může dědit nebo přepsat parametry její nadřazené organizace. Sdílené hlavní data, například výrobky a adresáře, však platí pro celou organizaci, a nelze je přepsat pro jednotlivé organizace.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>Doporučené postupy pro nastavování organizace v hierarchii

Při implementaci organizační hierarchie berte v úvahu následující doporučené postupy:
-   Vytvořte oddělení pro modelování průniku mezi právnickou osobu a obchodní jednotkou. Můžete pak také zahrnout data z oddělení do právnické osoby pro statutární vykazování a z oddělení do obchodní jednotky pro interní vytváření sestav.
-   U jedné právnické osoby nemodelujte více hierarchií pro stejný účel hierarchie.
-   Nevytvářejte hierarchii pro každý účel. Obvykle můžete použít jednu hierarchii pro několik účelů. Například jedna hierarchie provozních jednotek může být přiřazena ke všem účelům souvisejícím se zásadami.
-   Vytváření vyrovnaných hierarchií. V hierarchii všechny uzly, které jsou stejně vzdáleny od kořenového uzlu jsou definované jako úroveň. Ve vyrovnané hierarchii se může vyskytnout pouze jeden typ provozních jednotek a vzdálenost od kořenového uzlu ke každé úrovni je konzistentní. Jestliže jsou mezilehlé úrovně mezi oddělením a právnickou osobou nebo obchodní jednotkou, může být nutné vytvořit zástupné organizace pro vytvoření vyrovnané hierarchie.
-   Nemodeluje oddělenou hierarchii provozních jednotek, jestliže je struktura pro právnické osoby také vaší provozní strukturou. Smíšená hierarchie právnických osob a provozních jednotek může sloužit oběma účelům.
-   Před modelováním významných restrukturalizačních scénářů využijte data platnosti hierarchie k provedení analýzy dopadů a testu ověření.
-   Uložte hierarchii jako koncept, pokud je možnost, že změníte hierarchii před publikováním.
-   Omezte počet uživatelů, kteří mají oprávnění přidávat nebo odebírat organizace z hierarchie v produkčním prostředí. Menší počet snižuje riziko nákladné chyby a nutných oprav.

## <a name="retail-store-management"></a>Řízení maloobchodu
Následující tabulka popisuje scénáře modelu Základy obchodování pro použití organizačních hierarchií.
| Úkol                                                                           | Popis                                                                                                                                                                                                                                                                                                | Účel hierarchie    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Správa maloobchodních sortimentů                                                      | Určete výrobky, které jsou k dispozici v každém maloobchodě.                                                                                                                                                                                                                                             | Maloobchodní sortiment    |
| Správa maloobchodního doplňování                                                    | Seskupte obchody pro doplňování zásob na základě pravidel doplnění.                                                                                                                                                                                                                                          | Doplnění maloobchodu |
| Vykazování dat pro obchody                                                         | Seskupte obchody pro vykazování.                                                                                                                                                                                                                                                                                | Vykazování maloobchodu     |
| Zaúčtování zásob, počítání výkazů nebo zaúčtování výkazů pro skupinu obchodů | Vytvořte skupinu obchodů, která může být přiřazena do dávkové úlohy. Při definování dávkové úlohy pro zaúčtování zásob, vypočítání výkazů a zaúčtování výkazů můžete zadat, na kterou hierarchii úloha platí. Po přidání obchodů do nebo odebrání z hierarchie, musíte upravovat dávkovou úlohu. | Zaúčtování v Retail POS   |






