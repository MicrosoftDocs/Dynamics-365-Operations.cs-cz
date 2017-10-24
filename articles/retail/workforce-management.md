---
title: "Přehled služby Správa zaměstnanců"
description: "Toto téma popisuje použití služby Správa zaměstnanců (WFM) a využití známých výhod pokladního místa, moderního pokladního místa a cloudového pokladního místa, aby mohli manažeři obchodu snadno spravovat své zaměstnance."
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>Přehled služby Správa zaměstnanců

[!include[banner](includes/banner.md)]
    
Služba Správa zaměstnanců využívá známých výhod klientů pokladního místa (POS), moderního pokladního místa (POS) a cloudového pokladního místa (POS) a umožňuje manažerům obchodu snadno spravovat své zaměstnance. Služba WFM používá architekturu rozšíření ke stažení příslušných balíčků v POS. Tyto balíčky se stáhnou v okamžiku, kdy zavřete a znovu otevřete POS. Když tedy společnost Microsoft vydá nové funkce pro službu WFM, aplikaci POS je třeba zavřít a znovu otevřít.

Pomocí této služby manažeři obchodu mohou snadno vytvářet a publikovat týdenní pracovní plán pro své obchody. Zaměstnanci obchodu si mohou rychle zobrazit své vlastní plány a plány svých kolegů. Tímto způsobem se dozví, kdo s nimi bude pracovat během přiřazené směny. Zaměstnanci obchodu mohou také vytvořit požadavky na absenci, prohození směny a nabídku směny. Všechny tyto požadavky spustí definované workflow.

Během směny mohou zaměstnanci obchodu využít funkce příchodu a odchodu, která je součástí klientů POS. Data jsou následně odeslána do ústředí (HQ) pro zpracování mezd. Funkce příchodu a odchodu je existující funkce POS. Více informací o nastavení a podporovaných scénářích získáte v části [Příchod a odchod](retail-time-attendance.md).

## <a name="supported-scenarios"></a>Podporované scénáře
Tato část poskytuje více informací o podporovaných scénářích.

- **Vytváření a publikování plánů** – Služba WFM používá oprávnění POS, která jsou konfigurována v HQ k určení, zda má pracovník oprávnění manažera obchodu. Pouze manažeři obchodu mohou vytvářet a publikovat plány pomocí operace Správa plánu. Můžete rychle vytvořit plán pomocí kopírování a vkládání existující pracovní směny z jednoho pracovníka na jiného pracovníka. Pracovníci mohou také vytvořit plán pomocí importování plánu z jakéhokoliv předchozího týdne do aktuálního týdne.

    Pokud nebyl plán publikován, je ve stavu konceptu a vypadá jinak než publikovaný plán. Manažeři obchodu mohou publikovat plán kliknutím na tlačítko **Publikovat** pro libovolný týden. Poté, co je plán publikován na týden, jsou veškeré změny automaticky publikovány. Příklady změn zahrnují přidání nebo odstranění pracovních směn nebo absencí, nebo úpravy pracovních směn nebo absencí. Pracovníci obchodu si mohou zobrazit jen plány, které byly publikovány pro různé týdny.
    
- **Vytvoření a schválení požadavků** – Zaměstnanci obchodu mohou vytvořit tři typy požadavků:

    - Požadavek na absenci
    - Požadavek na prohození směny
    - Požadavek na nabídku směny

    Tyto požadavky lze vytvořit pomocí operace Požadavky na plán. Každý požadavek postupuje podle definovaného workflowu a zaměstnanci si mohou jednoduše zobrazit aktuální stav svých požadavků.
    
    Požadavky na absenci se automaticky odesílají manažerovi obchodu ke schválení. Pokud existuje více manažerů obchodu, všichni manažeři si mohou zobrazit daný požadavek, ale pouze jeden manažer ho může schválit nebo zamítnout. Typy absence se konfigurují v centrále pro maloobchod pomocí stránky **Typy pracovního volna a absence** v modulu **Retail**. Jakmile manažer obchodu schválí nebo zamítne požadavek, přesune se na kartu **Historie** pro operaci Požadavky na plán.
    
    Požadavek na přehození směn nebo nabídku směn odchází nejdříve pracovníkovi, kterému byl požadavek odeslán. Manažer obchodu si může zobrazit požadavek až poté, co ho schválil tento pracovník. Pokud tedy pracovník zamítne požadavek na prohození směny nebo požadavek na nabídku směny, vedoucí si ho nemůže zobrazit. Pracovník, který požadavek vytvořil, ho může také zrušit předtím, než ho manažer schválí nebo zamítne.

- **Zobrazení aktivních pracovníků obchodu v zobrazení plánu** – Když je pracovník přidán do obchodu, například jeho přiřazením k adresáři pracovníka obchodu, pracovník se stane dostupným pro plánování ve službě WFM. V HQ se spustí opakovaná dávková úloha s názvem **Zpracovat data pracovníka pro správu zaměstnanců**. Tato úloha připraví přiřazení pracovníka obchodu, která budou odeslána do služby Common Data Service (CDS).

    Stejný postup se použije, když je pracovník odebrán z obchodu. Pokud je však aktivní pracovní směna přiřazena pracovníkovi, zobrazuje se odebraný pracovník stále pro minulé, aktuální a budoucí týdny. Z toho vyplývá, že pokud nejsou tyto pracovní směny a absence smazány, odebraný pracovník se bude nadále zobrazovat pro tyto týdny.

