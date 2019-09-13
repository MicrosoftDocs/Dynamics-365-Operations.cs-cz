---
title: Prognózy, pracovní příkazy a projekty
description: Toto téma popisuje integraci prognóz a pracovních příkazů s modulem Řízení a účetnictví projektů ve Správě majetku.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886809"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognózy, pracovní příkazy a projekty

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Ve Správě majetku se provádí integrace s modulem **Řízení a účetnictví projektů** za účelem optimalizace řízení nákladů, což uživatelům umožňuje sledovat náklady v rámci prognóz typů prací údržby a úloh pracovních příkazů.

Chcete-li sledovat prognózu typu prací údržby, je nutné provést dvě nastavení:

1. Přejděte do **Správa majetku** > **Nastavení** > **Parametry správy majetku** > odkaz **Majetek** > záložka s náhledem **Projekt** > pole **Projekt prognózy údržby**.

2. V části **Výchozí nastavení typu práce údržby** při vytvoření výchozího řádku typu práce údržby je automaticky vytvořeno číslo aktivity pro daný řádek (**Správa majetku** > **Nastavení** > **Práce** > **Výchozí nastavení typu práce**).

Prognózy typu práce údržby slouží dvěma účelům: v modulu **Řízení a účetnictví projektů** můžete sledovat náklady na prognózy typů prací údržby. Prognózy se dále automaticky přenesou do projektu úlohy pracovního příkazu při výběru typu práce údržby na pracovním příkazu.

Chcete-li sledovat náklady na úlohy pracovních příkazů, musíte nejprve nastavit projekty pracovních příkazů. Popis potřebného postupu naleznete v části [Nastavení projektu pracovního příkazu](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Projekty úloh pracovních příkazů

Při vytváření úlohy pracovního příkazu na pracovním příkazu je projekt pracovního příkazu určen nastavením nadřazeného projektu pro pracovní příkazy v sekci **Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Nastavení projektu**.

Projekty úloh pracovních příkazů jsou vytvářeny pomocí kombinace následujících informací o pracovním příkazu:

- Typ pracovního příkazu vybraný na pracovním příkazu 
- Funkční místo související s majetkem v úloze pracovního příkazu
- Typ majetku související s majetkem v úloze pracovního příkazu  
- Očekávaný čas zahájení a ukončení nastavený na pracovním příkazu  

Je možné, že ne všechny výše uvedené informace se nacházejí v pracovním příkazu. Vyhledávání nadřazeného projektu pracovního příkazu je proto provedeno pomocí dostupné kombinace dat a výběrem ID projektu, které odpovídá údajům pracovního příkazu.

Příklad: Na níže uvedeném obrázku je nastavení typu majetku „Motor nákladního automobilu“ znamená, že každá úloha pracovního příkazu vytvořená s tímto typem majetku bude dílčím projektem pro ID projektu „000186“.

![Obrázek č. 1](media/01-integration-to-pma.png)

Účelem ID projektu v úloze pracovního příkazu a souvisejícího čísla aktivity (**Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** > v seznamu vyberte pracovní příkaz > záložka s náhledem **Podrobnosti řádku** > pole **ID projektu** a pole **Číslo aktivity**) je sledování nákladů souvisejících s úlohou pracovního příkazu a majetku vybraného v úloze pracovního příkazu v modulu **Řízení a účetnictví projektů**. 

Na následujícím obrázku je zobrazen grafický přehled projektů pracovních příkazů a souvisejících aktivit projektu.

![Obrázek č. 2](media/02-integration-to-pma.png)

Při vytvoření nové úlohy pracovního příkazu na pracovním příkazu je automaticky vytvořen projekt pracovního příkazu pro danou úlohu. Finanční dimenze majetku souvisejícího s úlohou pracovního příkazu se automaticky přenesou do projektu pracovního příkazu. Aktivita projektu vytvořená pro úlohu pracovního příkazu obsahuje související informace týkající se typu práce údržby, typu operace údržby a obchodu. Tyto údaje jsou užitečné, pokud například vytvoříte nákupní objednávku z pracovního příkazu (viz [Zásobování](../work-orders/procurement.md)) nebo pokud pro registraci pracovní doby používáte modul **Řízení a účetnictví projektů**.  

Pokud byl majetek instalován ve funkčním místě a tento majetek je později nainstalován v jiném funkčním místě, finanční dimenze majetku související s novým funkčním místem se automaticky aktualizují. Poté, když pro daný majetek vytvoříte úlohu pracovního příkazu, projekt pracovního příkazu pro úlohu pracovního příkazu automaticky získá finanční dimenze, které aktuálně souvisejí s majetkem. To znamená, že při použití funkčních míst mohou být náklady vždy sledovány ve funkčních místech, ve kterých byl majetek nainstalován v daném okamžiku. Automatická aktualizace finančních dimenzí zajišťuje úplnou sledovatelnost nákladů pro řízení a vykazování projektů.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Projekty s pracovními příkazy, stavy životního cyklu pracovních příkazů, fáze projektu a typy projektů

Chcete-li zajistit správné používání stavů životního cyklu pracovních příkazů a souvisejících fází projektu v pracovních příkazech, zvažte závislosti na modulu **Řízení a účetnictví projektů**:

- V modulu **Řízení a účetnictví projektů** se fáze projektu nastavují pro typy projektů v části **Parametry řízení a účetnictví projektů**.  
- V části **Parametry řízení a účetnictví projektů** nezapomeňte zaškrtnout příslušná políčka fáze projektu pro všechny typy projektů, které hodláte použít. Na níže uvedeném obrázku jsou pro typy projektů „Čas a materiál“ a „Interní“ vybráno pět fází: **Vytvořeno** - **Odhad** - **Rozvrh** - **Zpracování** - **Dokončeno**. Těchto pět fází souvisí s interními pracemi údržby i servisními pracemi údržby.  
- V modulu **Správa majetku** jsou typy projektů definovány skupinami projektů, které nastavíte ve formuláři **Nastavení projektu pracovního příkazu** > odkaz **Skupina projektů**.  
- Nastavení skupin projektů v **Nastavení projektu pracovního příkazu** se používá při vytváření pracovních příkazů. Při vytvoření pracovního příkazu je pro daný pracovní příkaz automaticky vytvořen projekt pracovního příkazu.  
- Každý stav životního cyklu pracovního příkazu musí mít související fázi projektu.  
- Fáze projektu související se stavem životního cyklu pracovního příkazu musí být definována jako aktivní fáze pro skupinu projektů definovanou v projektu pracovního příkazu. Projekt pracovního příkazu je automaticky vytvořen v rámci pracovního příkazu.  
- Při vytvoření nového pracovního příkazu je automatické přidělení projektu pracovního příkazu založeno na **nastavení projektu pracovního příkazu** (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Nastavení projektu**).  

Následující obrázky znázorňují přidružení mezi skupinami projektů pracovních příkazů, typy souvisejících projektů, fázemi projektu a stavy životního cyklu pracovního příkazu.  

![Obrázek č. 3](media/03-integration-to-pma.png)

![Obrázek č. 4](media/04-integration-to-pma.png)

![Obrázek č. 5](media/05-integration-to-pma.png)

V části [Nastavení projektu pracovního příkazu](../setup-for-work-orders/work-order-project-setup.md) najdete informace, jak nastavit projekty pracovních příkazů, a v části [Stavy životního cyklu pracovního příkazu](../setup-for-work-orders/work-order-lifecycle-states.md) zjistíte, jak vytvořit stavy životního cyklu pracovních příkazů.

Na následujícím obrázku je znázorněn grafický přehled různých projektů vytvořených v modulu **Správa majetku**, které umožňují integraci s modulem **Řízení a účetnictví projektů**, a také o pracovních procesech souvisejících s projekty.

![Obrázek č. 6](media/06-integration-to-pma.png)

