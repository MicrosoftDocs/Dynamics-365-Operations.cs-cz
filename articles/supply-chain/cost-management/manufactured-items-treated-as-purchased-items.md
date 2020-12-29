---
title: Nastavení produktů, které mohou být vyrobeny nebo pořízeny
description: Produkty mohou být odebírány různými způsoby – mohou být produkovány (vyrobeny) nebo získané (nakupované). Tento článek popisuje některé typické body, které je třeba zvážit při konfiguraci produktů pro podporu více zdrojů.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9b5ba58703e636308d83a94ecc2e27e44812c49
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423865"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a>Nastavení produktů, které mohou být vyrobeny nebo pořízeny

[!include [banner](../includes/banner.md)]

Produkty mohou být odebírány různými způsoby – mohou být produkovány (vyrobeny) nebo získané (nakupované). Tento článek popisuje některé typické body, které je třeba zvážit při konfiguraci produktů pro podporu více zdrojů. 

Získávání z více zdrojů se obvykle používá k zakoupení položky, která je příležitostně vyráběna, nebo v případě, že položka byla především vyráběna a byla změněna, takže je aktuálně převážně kupovaná. Daná položka je nejprve označena jako vyráběná položka s cílem definování údajů kusovníku a údajů o postupu nebo s cílem podpory výrobních zakázek pro danou položku. Typ výroby je třeba nastavit na **Kusovník** (nebo pro výrobní proces **Vzorec** nebo **Souběžný produkt**).

Při použití standardních nákladů lze pro vyráběnou položku vypočítat záznam o nákladech položky. Záznam o nákladech na položku však nemusí odpovídat standardním nákladům, které požadujete pro účely nákupu. V tomto případě je nutno standardní náklady ručně zadat a aktivovat pro záznam o nákladech na položku. Pro výpočet nákladů zvažte použití zvláštního kusovníku a postupu, který představuje kombinaci zásobování produktu v průběhu fiskálního období za účelem minimalizace odchylek během určité doby. Položku vyráběnou na jednom pracovišti lze také převést na jiné pracoviště. Z toho vyplývá, že náklady na položku je nutné ručně zadat a aktivovat pro pracoviště, na které položka převádí. Pokud vyráběnou položku použijete jako komponentu pro výrobky vyšší úrovně, je třeba s náklady na tuto komponentu pracovat jako se zakoupenou položkou. Tato směrnice platí bez ohledu na to, zda náklady komponenty byly vypočteny nebo ručně zadány. To znamená, že výpočet kusovníku musí pracovat s náklady na položku jako se zakoupenou komponentou namísto použití údajů o kusovníku a postupu položky k výpočtu nákladů. 

Výpočtu lze předejít výběrem příznaku **Zastavit rozpad**, který je vložen do skupiny výpočtu kusovníku přiřazené k dané položce. Chcete-li zabránit požadavkům na rozpad u výpočtů hlavního plánování prostřednictvím položky, nastavte ochrannou dobu rozpadu na hodnotu 0 (nula) dní pro disponibilitu položky nebo ve skupině disponibility. Kalkulace hlavního plánování bude pracovat s položkou jako s nakoupenou položkou a nebudou prováděny další výpočty pro údaje o kusovníku a postupu položky.





