---
title: Přehled verzí výpočtu nákladů
description: Tento článek obsahuje informace o nákladových verzích, způsobu jejich udržování a typech dat, která lze do nich zahrnout. Hlavním účelem nákladové verze je to, že obsahuje záznamy o položkách, kategorie nákladů a vzorce pro výpočet nepřímých nákladů.
author: AndersGirke
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "54532"
- intro-internal
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3fa4f14d6a6b5afe6bb58f94f636be58ea2e721e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565968"
---
# <a name="costing-versions-overview"></a>Přehled verzí výpočtu nákladů

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o nákladových verzích, způsobu jejich udržování a typech dat, která lze do nich zahrnout. Hlavním účelem nákladové verze je to, že obsahuje záznamy o položkách, kategorie nákladů a vzorce pro výpočet nepřímých nákladů.

Nákladová verze slouží jednomu nebo více účelům podle toho, jaká data obsahuje. Hlavním účelem nákladové verze je to, že obsahuje záznamy o položkách, kategorie nákladů a vzorce pro výpočet nepřímých nákladů. Nákladová verze může obsahovat sadu záznamů o standardních nákladech nebo sadu záznamů o plánovaných nákladech založených na nákladovém typu, který je přiřazený nákladové verzi.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Nákladové verze pro standardní nebo plánované náklady
### <a name="standard-costs"></a>Standardní náklady

Nákladová verze může podporovat model standardních skladových nákladů položek, kdy nákladová verze obsahuje sadu záznamů o standardních nákladech položek a výrobních postupů. Údaje o nákladech výrobních postupů jsou vyjádřeny prostřednictvím kategorií nákladů pro operace technologického postupu a vzorců pro výpočet výrobní režie.

### <a name="planned-costs"></a>Plánované náklady

Nákladová verze může obsahovat sadu záznamů o plánovaných nákladech položek a výrobních postupů. Nákladová verze s plánovanými náklady se často používá při simulovaných výpočtech nákladů, jako je například simulace vlivu změn nákladů na nakupovaný materiál nebo simulace dopadu změn ve výrobních postupech na kalkulované náklady vyrobených položek. Záznamy o cenách položek pro plánované náklady lze rovněž využít k podpoře modelu skutečných skladových nákladů poskytnutím počátečních hodnot pro ceny položek. Tyto hodnoty zahrnují výpočet plánovaných nákladů pro vyráběné položky.

## <a name="entering-costs"></a>Zadání nákladů
Údržba dat záznamů o cenách v nákladové verzi spočívá v zadávání cen pro nakoupené položky a pro položky, které se převádějí mezi pracovišti. U výrobců zahrnuje další údržba dat zadávání nákladů pro kategorie nákladů, které jsou přidruženy k operacím postupů, zadávání vzorců pro výpočet nepřímých nákladů, které odrážejí výrobní režii, a výpočet nákladů na vyrobené položky. 

Data o cenách položek v nákladové verzi obsahují jeden nebo více záznamů o ceně pro každou položku. Záznam o ceně položky má po vložení stav **Čeká na zpracování** a zamýšlené datum účinnosti. Když záznamu o ceně položky aktivujete, změní se jeho stav na **Aktivní** a datum účinnosti se změní na datum aktivace. Různé záznamy o nákladech na položku mohou být důsledkem různých pracovišť, dat účinnosti nebo stavů. Při kalkulaci nákladů na vyrobené položky k budoucímu datu se pro výpočet kusovníku použijí záznamy o cenách s příslušným datem účinnosti bez ohledu na to, zda mají stav **Čeká na zpracování** nebo **Aktivní**. Při odhadu nákladů na výrobní zakázku a oceňování skladových transakcí se u modelu standardních skladových nákladů použije aktivní záznam o aktuální ceně položky. Správa záznamů o cenách pro kategorie nákladů a vzorců pro výpočet nepřímých nákladů je podobná jako správa záznamů o cenách položek. 

Pro nákladové verze existují dvě zásady blokování, které určují, zda může probíhat údržba čekajících nákladů a zda čekající náklady mohou být aktivovány. Zásady blokování použijte k povolení správy dat a poté k zakázání správy dat pro záznamy o cenách v nákladové verzi. 

Nákladová verze může pro účely výpočtu kusovníku dále obsahovat data o prodejních nebo nákupních cenách položek.

## <a name="item-sales-prices-for-bom-calculations"></a>Prodejní ceny položek pro výpočty kusovníku
Hlavním důvodem pro zahrnutí dat o prodejních cenách je uchování vypočtených prodejních cen pro vyrobené položky. Vypočtenou prodejní cenu je pak možné analyzovat a zjistit, jak komponenty, operace postupu a režie přispívají k nákladové a prodejní ceně. 

Druhým důvodem pro zahrnutí dat o prodejních cenách je definování záznamů o prodejních cenách pro položky komponenty. Tyto záznamy můžete použít k výpočtu prodejní ceny vyráběných položek. Nejprve definujte model prodejních cen, který je vložen ve skupině výpočtu kusovníku, a přiřaďte skupinu výpočtu kusovníku k nakupovaným položkám. Poté při provádění výpočtů kusovníku, které používají plánované náklady, vyberte model nákladových cen skupiny výpočtu kusovníku. 

Jinak se záznamy o prodejní ceně položek používají pouze jako referenční informace bez ohledu na to, zda jsou záznamy zadány ručně, nebo vypočteny. Aktivací záznamu o prodejní ceně položky můžete změnit základní prodejní cenu položky. Základní prodejní cena však není specifická pro pracoviště a lze ji ručně přepsat. Základní prodejní cena položky slouží jako výchozí prodejní cena v prodejních objednávkách a prodejních nabídkách.

## <a name="item-purchase-prices-for-bom-calculations"></a>Nákupní ceny položek pro výpočty kusovníku
Hlavním důvodem pro povolení dat o nákupní ceně je definování záznamů o nákupních cenách pro položky komponent, aby bylo možné tyto záznamy využít k výpočtu nákladů na vyráběné položky. Záznamy o nákupních cenách položek je nutné zadat ručně. 

Chcete-li povolit obsah nákupních cen, je nutné nejprve určit skupinu výpočtu kusovníku, která obsahuje model nákladových cen pro nákupní ceny položky, a přiřadit skupinu výpočtu kusovníku k zakoupeným položkám. Model nákladových cen poté použijete pro skupinu výpočtu kusovníku při provádění výpočtů kusovníku, který k výpočtu prodejních cen vyráběných položek využívá plánované náklady . 

Záznamy o nákupních cenách pro položky slouží také jako referenční informace. Změnou stavu záznamu o nákupní ceně položky z hodnoty **Čeká na zpracování** na hodnotu **Aktivní** můžete změnit základní nákupní cenu položky. Základní nákupní cena však není specifická pro pracoviště a lze ji ručně přepsat. Základní nákupní cena položky slouží jako výchozí nákupní cena na nákupních objednávkách.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]