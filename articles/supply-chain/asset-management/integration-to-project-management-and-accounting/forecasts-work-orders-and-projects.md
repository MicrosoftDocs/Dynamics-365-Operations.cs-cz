---
title: Prognózy, pracovní příkazy a projekty
description: Toto téma popisuje integraci prognóz a pracovních příkazů s modulem Řízení a účetnictví projektů ve Správě majetku.
author: josaw1
manager: AnnBe
ms.date: 08/29/2019
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
ms.openlocfilehash: cc1992326c448ee8dc30a9ad8f8f538ebea83e54
ms.sourcegitcommit: f853c8d46ffc8e578387bac4cd48a948916983ef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/19/2019
ms.locfileid: "2002377"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognózy, pracovní příkazy a projekty

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Ve Správě majetku se provádí integrace s modulem **Řízení a účetnictví projektů** pro pomoc s optimalizací řízení nákladů, aby mohli uživatelé sledovat náklady v rámci prognóz typů prací údržby a úloh pracovních příkazů.

Sledování prognózy typu prací údržby vyžaduje dvě nastavení:

1. Vyberte projekt v **Správa majetku** > **Nastavení** > **Parametry správy majetku** a pak na kartě **Majetek** > na pevné záložce **Projekt** v poli **Projekt prognózy údržby** vyberte projekt.

2. Při vytvoření výchozího řádku typu práce údržby je automaticky vytvořeno číslo aktivity pro daný řádek na stránkce **Výchozí nastavení typu práce údržby** (**Správa majetku** > **Nastavení** > **Práce** > **Výchozí nastavení typu práce**).

Prognózy typu úlohy údržby slouží dvěma účelům: 

- V modulu **Řízení projektů a účetnictví** můžete sledovat náklady na prognózy typů úloh údržby. 
- Prognózy se automaticky přenesou do projektu úlohy pracovního příkazu při výběru typu práce údržby na pracovním příkazu.

Chcete-li sledovat náklady na úlohy pracovních příkazů, musíte nejprve nastavit projekty pracovních příkazů. Další informace naleznete v tématu [Nastavení projektu pracovního příkazu](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Projekty úloh pracovních příkazů

Při vytváření úlohy pracovního příkazu na pracovním příkazu je projekt pracovního příkazu určen nastavením nadřazeného projektu pro pracovní příkazy na stránce **Nastavení projektu pracovního příkazu** (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Nastavení projektu**).

Projekty úloh pracovních příkazů jsou vytvářeny pomocí kombinace následujících informací o pracovním příkazu:

- Typ pracovního příkazu vybraný na pracovním příkazu 
- Funkční místo související s majetkem v úloze pracovního příkazu
- Typ majetku, který souvisí s majetkem v úloze pracovního příkazu  
- Očekávané časy zahájení a ukončení nastavené na pracovním příkazu  

Některé z těchto informací nemusí být v pracovním příkazu nalezeny. Vyhledávání nadřazeného projektu pracovního příkazu je proto provedeno pomocí dostupné kombinace dat a výběrem ID projektu, které odpovídá údajům pracovního příkazu.

Na následujícím obrázku, vzhledem ke způsobu nsatavení typu majetku **Motor n ákladního automobilu**, bude každá úloha pracovního příkazu, která je vytvořena s typem majetku **Motor nákladního automobilu** dílčím projektem ID projektu 000186.

![Obrázek č. 1](media/01-integration-to-pma.png)

Účelem ID projektu na úloze pracovního příkazu a čísla související aktivity je sledování nákladů, které souvisejí s úlohou pracovního příkazu, a majetku, který je na něm vybrán, v modulu **Řízení projektů a účetnictví**. (Chcete-li zobrazit ID projektu a číslo aktivity, vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** a poté vyberte požadovaný pracovní příkaz. Na pevné záložce **Podrobnosti řádku** pole **ID projektu** obsahuje ID projektu a pole **Číslo aktivity** obsahuje číslo aktivity.) Další informace o řízení nákladů v modulu Správa majetku naleznete v [Kontrola data a nákladů](../controlling-and-reporting/cost-and-date-control.md).

Na následujícíilustraci je zobrazen grafický přehled projektů pracovních příkazů a souvisejících aktivit projektu.

![Obrázek č. 2](media/02-integration-to-pma.png)

Při vytvoření nové úlohy pracovního příkazu na pracovním příkazu je automaticky vytvořen projekt pracovního příkazu pro danou úlohu. Finanční dimenze majetku, které souvisí s úlohou pracovního příkazu, se automaticky přenesou do projektu pracovního příkazu.

Aktivita projektu, která je vytvořena pro úlohu pracovního příkazu, souvisí s připojenými informacemi. Tyto informace se týkají typu úlohy údržby, varianty typu údržby a obchodu. Jsou užitečné, pokud například vytvoříte nákupní objednávku z pracovního příkazu (viz [Zásobování](../work-orders/procurement.md)) nebo pokud pro registraci pracovní doby používáte modul **Řízení a účetnictví projektů**.

Pokud byl majetek instalován ve funkčním místě, ale tento majetek je později nainstalován v jiném funkčním místě, finanční dimenze, které souvisí s novým funkčním místem, se na majetku automaticky aktualizují. Pak, když pro daný majetek vytvoříte úlohu pracovního příkazu, projekt pracovního příkazu pro úlohu pracovního příkazu automaticky získá finanční dimenze, které aktuálně souvisejí s majetkem. To znamená, že při použití funkčních míst mohou být náklady vždy sledovány ve funkčních místech, ve kterých byl majetek nainstalován v daném okamžiku. Automatická aktualizace finančních dimenzí pomáhá zajistit úplnou sledovatelnost nákladů pro řízení a vykazování projektů.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Projekty s pracovními příkazy, stavy životního cyklu pracovních příkazů, fáze projektu a typy projektů

Chcete-li pomoci zajistit správné používání stavů životního cyklu pracovních příkazů a souvisejících fází projektu v pracovních příkazech, zvažte závislosti na modulu **Řízení a účetnictví projektů**:

- V modulu **Řízení a účetnictví projektů** se fáze projektu nastavují pro typy projektů na stránce **Parametry řízení a účetnictví projektů**.  
- Na stránce **Parametry řízení a účetnictví projektů** pomocí příslušných políček fáze vyberte relevantní fáze projektu pro všechny typy projektů, které hodláte použít. Na následujících obrázcích bylo vybráno pět fází (**Vytvořeno**, **Odhad**, **Naplánováno**, **Zpracování** a **Dokončeno**) pro typy projektů **Čas a materiál** a **Interní**. Těchto pět fází souvisí s interními pracemi údržby i servisními pracemi údržby.
- V modulu **Správa majetku** jsou typy projektu definovány skupinami projektů, které nastavíte na stránce **Nastavení projektu pracovního příkazu** > karta **Skupina projektu** (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Nastavení projektu**).  
- Nastavení skupin projektů na stránce **Nastavení projektu pracovního příkazu** se používá při vytváření pracovních příkazů. Při vytvoření pracovního příkazu je pro daný pracovní příkaz automaticky vytvořen projekt pracovního příkazu.  
- Každý stav životního cyklu pracovního příkazu musí mít související fázi projektu.  
- Fáze projektu související se stavem životního cyklu pracovního příkazu musí být definována jako aktivní fáze pro skupinu projektů definovanou v projektu pracovního příkazu. Projekt pracovního příkazu je automaticky vytvořen v rámci pracovního příkazu.
- Při vytvoření nového pracovního příkazu je automatické přidělení projektu pracovního příkazu založeno na nastavení na stránce **Nastavení projektu pracovního příkazu**.  

Následující obrázky znázorňují přidružení mezi skupinami projektů pracovních příkazů, typy souvisejících projektů, fázemi projektu a stavy životního cyklu pracovního příkazu.

![Obrázek č. 3](media/03-integration-to-pma.png)

![Obrázek č. 4](media/04-integration-to-pma.png)

![Obrázek č. 5](media/05-integration-to-pma.png)

Další informace o nastavení projektů pracovních příkazů naleznete v tématu [Nastavení projektu pracovního příkazu](../setup-for-work-orders/work-order-project-setup.md). Další informace o tom, jak vytvořit stavy životního cyklu pracovního příkazu naleznete v tématu [Stavy životního cyklu pracovního příkazu](../setup-for-work-orders/work-order-lifecycle-states.md).

Na následujícím obrázku je znázorněn grafický přehled různých projektů vytvořených v modulu **Správa majetku**, které umožňují integraci s modulem **Řízení projektů a účetnictví**. Dále jsou zde uvedeny pracovní procesy, s kterými souvisí projekty.

![Obrázek č. 6](media/06-integration-to-pma.png)

