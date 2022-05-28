---
title: Konfigurace parametrů pro automatizaci procesu inkasa
description: Toto téma popisuje parametry, které ovlivňují procesy automatizovaného inkasa, a poskytuje pokyny pro jejich nastavení, aby automatizovaný proces odrážel vaše záměry a očekávání.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e7a7e048a371fc90456368206b91c29c4b1264d5
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734389"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Konfigurace parametrů pro automatizaci procesu inkasa

[!include [banner](../includes/banner.md)]

Toto téma popisuje parametry, které ovlivňují procesy automatizovaného inkasa, a poskytuje pokyny pro jejich nastavení, aby automatizovaný proces odrážel vaše záměry a očekávání. Informace o tom, jak automatizovat procesy inkasa, najdete v tématu [Automatizace procesů inkasa](collections-process-automate.md).

## <a name="general"></a>Obecný
Zadejte číslo do pole **Procento zákazníků na dávkový úkol**, které určuje počet dávkových úloh na proces automatizace. Nastavte možnost **Automatické zaúčtování upomínek** na **Ano**, aby typ akce upomínky zaúčtoval dopis během automatizace. Nastavte možnost **Vytvářet aktivity pro automatizace** na **Ano**, aby se vytvářely a uzavíraly aktivity pro typy akcí bez aktivity a zobrazily se všechny automatizované kroky provedené na účtu. Počet dní, po které je historie inkasa uložena, se definuje v poli **Dny uchování historie automatizace procesů inkasa**. Když faktura dosáhne posledního kroku procesu inkasa, nebude použita k vytvoření typů akcí budoucí automatizace procesů, pokud je možnost **Vyloučit fakturu po aktivaci posledního kroku procesu** nastavena na **Ano**. Další nejstarší faktura určí další krok automatizace procesu, aby bylo zajištěno, že akce automatizace procesu shromažďování budou pokračovat. 

## <a name="payment-predictions"></a>Předpovědi plateb
Počínaje verzí 10.0.21, předpovědi plateb od zákazníků, nalezené v Finance Insights, ukazuje, zda bude faktura zaplacena včas, pozdě nebo velmi pozdě. Každou z těchto kategorií můžete konfigurovat v aplikaci Finance Insights. Pokud se předpokládá opožděné zaplacení faktur, je důležité zahájit proces inkasa před splatností faktury. Tyto předpovědi lze použít k vytváření aktivit inkasa, když běží automatizace procesů inkasa. Nastavte možnost **Povolit předpovědi plateb** na **Ano**, aby předpovědi plateb zákazníků byly použity k vytváření aktivit inkasa na základě pravděpodobnosti, že faktura bude zaplacena pozdě. 

Další informace o předpovědích plateb zákazníků a Finance Insights najdete v části [Předpovědi plateb zákazníků](payment-insights-overview.md).

Když se spustí model předpovědi plateb zákazníka, přiřadí procento k předpovědi platby faktury včas, pozdě nebo velmi pozdě. Tyto informace můžete použít k automatickému zahájení aktivit inkasa pomocí automatizace procesů inkasa v případech, kdy se očekává pozdní platba. Tato procenta můžete zobrazit na stránkách **Předpovědi plateb za zákazníka** nebo **Předpovědi plateb za transakci** v části **Kredit a inkasa > Inkasa**. 

Pokud je předpověď průměrné platby pro zákaznickou fakturu menší než referenční procento, nevytvoří se žádná aktivita. Pokud je předpověď faktury větší nebo rovná referenčnímu procentu, vytvoří se jedna aktivita na zákazníka. Pro variantu **Předpověď: Pozdě** zadejte **Referenční procento** určující, kdy by automatizace procesů inkasa měla vytvářet aktivity inkasa. Toto je souhrnná hodnota pro varianty pozdě i velmi pozdě. Vyberte **Šablonu obchodního dokumentu**, která se použije pro vytvořenou aktivitu nebo vytvoření nové aktivity. Toto identifikuje **Typ**, **Účel** a **Dny do ukončení činnosti**. Zadejte libovolné **Poznámky**, které budou výchozím popisem při vytvoření aktivity. Pro variantu **Předpověď: Velmi pozdě** zadejte **Referenční procento** určující, kdy by automatizace procesů inkasa měla vytvářet aktivity inkasa pro zákazníka s předpovědí velmi pozdního zaplacení faktur. Vyberte **Šablonu obchodního dokumentu**, která se použije pro vytvořenou aktivitu. Toto identifikuje **Typ**, **Účel** a **Dny do ukončení činnosti**. Zadejte libovolné **Poznámky**, které budou výchozím popisem při vytvoření aktivity. 

### <a name="example"></a>Příklad
Pokud je referenční procento varianty Pozdě nastaveno na 60%. Když se spustí předpovědi plateb zákazníka pro každou fakturu, systém přiřadí procento k předpovědi platby včas, pozdě nebo velmi pozdě. Pokud předpověď platby říká, že faktura bude zaplacena pozdě s pravděpodobností 59 % nebo méně, nebude pro fakturu automatizovaným procesem inkasa vytvořena žádná aktivita inkasa. Pokud je předpověď platby zákazníka pro fakturu větší nebo rovna 60 %, vytvoří se aktivita inkasa během automatizace procesu inkasa. 

> [!NOTE]
> Předpověď velmi pozdní platby je vyhodnocena před předpovědí pozdní platby, protože varianta velmi pozdně zahrnuje faktury, u nichž se předpokládá pozdní zaplacení. Proces inkasa generuje pouze jednu aktivitu, pokud faktura spadá do pásma pozdní i velmi pozdní platby. V takovém případě systém používá velmi pozdní aktivitu a obchodní dokument, protože varianta velmi pozdě má vyšší prioritu. Jakékoli další akce, které již byly vygenerovány, nebudou generovány podruhé.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
