---
title: Nákladové kategorie použité ve výrobních postupech
description: Tento článek obsahuje informace o nákladových kategoriích, které se týkají výrobních prostředí využívající trasování.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f36154467f7d392f9bb77bf907807d8acc4f61ff
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679520"
---
# <a name="cost-categories-used-in-production-routing"></a>Nákladové kategorie použité ve výrobních postupech

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o nákladových kategoriích, které se týkají výrobních prostředí využívající trasování.

Nákladové kategorie se týkají výrobních prostředí, v nichž jsou použity postupy. Jsou přiřazeny k provozním prostředkům a operacím postupu s cílem definovat hodinové náklady a rozdělení nákladových příspěvků do segmentů v rámci vypočtených nákladů na vyráběnou položku. Pro nákladové skupiny, které jsou přiřazeny k nákladovým kategoriím, jsou výrobní nákladové příspěvky klasifikovány na základě provozních prostředků a typu aktivity (například čas přípravy a operační čas). Specifikace přidělení nákladových skupin poskytuje základ pro výpočet režijních nákladů na výrobu na základě informací postupu. 

**Poznámka:** Ve výrobních prostředích jsou nákladové kategorie pojmenovány podle různých názvů (například kódy sazby práce nebo kódy strojových sazeb). 

S každou nákladovou kategorií jsou asociovány záznamy nákladů a je k ní přiřazena nákladová skupina. Pro různé výrobní účely jsou potřeba různé nákladové kategorie.

-   Přiřaďte různé hodinové náklady v závislosti na provozním prostředku. Náklady se mohou náklady lišit pro různé typy pracovních dovedností, zařízení nebo výrobní buňky.
-   Proveďte přiřazení různých hodinových nákladů pro čas přípravy a operační čas, které jsou asociovány s určitou operací postupu.
-   Proveďte přiřazení provozních prostředků podle výstupního množství, namísto hodinových nákladů (například sazby za kus pro mzdy pracovníků).
-   Poskytuje rozdělení skupin nákladů pro příspěvky nákladů do vypočítaných nákladů vyráběné položky. Například můžete rozdělit práci a strojní náklady.
-   Určete základ nákladové skupiny pro výpočetní vzorce režijních nákladů, jako jsou například vzorce pro režijní náklady související s pracovními silami a se strojovým vybavením nebo režijní náklady související s časem přípravy a operačním časem.

Nákladovou kategorii lze přidělit k času přípravy, operačnímu času a k množství pro operaci postupu. Pokud se například segmentace nákladů a nákladových skupin mezi časem přípravy a operačním časem liší, je třeba definovat a přiřadit různé nákladové kategorie pro čas přípravy a operační čas. Selektivní použití nákladových kategorií pro čas přípravy, čas zpracování a množství je určeno skupinou postupu, která je přiřazena k určité operaci. Přiřazení nákladových kategorií k časovým údajům a množství může být povinné v závislosti na podnikových zásadách, které jsou vloženy na stránce **Parametry modulu Řízení výroby**. 

Ke každé nákladové kategorii jsou přiřazeny náklady na základě definice záznamů nákladů v rámci nákladové verze. Použijte stránku **Cena nákladové kategorie** pro definování záznamů nákladů pro konkrétní nákladovou verzi a pracoviště. Záznam nákladů pro nákladovou kategorii je nejprve zadán se stavem **Nevyřízeno** a určeným datem platnosti. Když záznamu o ceně položky aktivujete, změní se jeho stav na **Aktuálně aktivní** a datum účinnosti se změní na datum aktivace. Různé záznamy o nákladech mohou být důsledkem různých pracovišť, dat účinnosti nebo stavů. Ve výpočtech kusovníku pro budoucí nebo minulá data budou použity záznamy nákladů s odpovídajícím datem platnosti. Aktuální aktivní záznam nákladů bude použit pro odhad nákladů výrobní zakázky a pro vyhodnocení ohlášené doby oproti výrobní zakázce. 

Záznam nákladů pro nákladovou kategorii může být specifický pro určité pracoviště nebo může být platný v rámci celé společnosti. Chcete-li záznam o nákladech vytvořit pouze pro dané pracoviště, pracoviště k ní přiřaďte. V opačném případě bude prázdná hodnota znamenat, že daný záznam nákladů bude použit pro všechna pracoviště v rámci společnosti. Náklady se mohou například mezi různými pracovišti lišit, takže bude nutné záznamy nákladů definovat jako specifické podle pracovišť. 

Pro operaci postupu jsou obvykle zděděny nákladové kategorie, které jsou přiřazeny k provoznímu prostředku nebo k hlavní operaci. Pokud vytváříte výrobní zakázku, budou operace postupu v rámci výrobního postupu odrážet vybranou verzi postupu. Nákladové kategorie přiřazené k operacím v rámci výrobního postupu můžete přepsat. 

Některé typy výrobní práce se mohou vztahovat na odhadovaný čas projektu a zprávy. Nákladová kategorie v tomto případě je nutná pro účely výroby a projektu. Je-li určitá nákladová kategorie označena příznakem pro použití v projektech, je nutné definovat další informace související s daným projektem.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]