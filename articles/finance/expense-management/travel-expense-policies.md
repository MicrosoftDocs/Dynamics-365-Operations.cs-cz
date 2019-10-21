---
title: Definice zásad výdajů
description: Můžete definovat zásady výdajů, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek v aplikaci Microsoft Dynamics 365 Finance.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d3b4a8f6cf74bb1fe7e53a4dfdd607f604e16e3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187445"
---
# <a name="define-expense-policies"></a>Definice zásad výdajů

[!include [banner](../includes/banner.md)]

Můžete definovat zásady, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek.         
Implementací zásad výdajů budete moci efektivně spravovat výdaje.         

Můžete například nastavit zásadu pro výdaje za hotel v New Yorku, která stanoví, že výdaje nesmí přesáhnout 250 USD za jeden nocleh.       
Pokud pracovník odešle sestavu výdajů nebo cestovní žádanku, ve kterém sazba za pokoj přesáhne tuto částku, systém oznámí        
pracovníkovi, že částka zásad pro výdaje byla překročena Můžete konfigurovat zprávu, kterou zaměstnanec obdrží při        
definování zásady.      
        
Můžete definovat tři typy zásad:         
        
- Upozornění - Umožňuje pracovníkovi odeslat výkaz výdajů nebo cestovní žádanku, ale výdaje budou označeny pro všechny schvalující osoby a        
  pro pozdější vykazování.        

- Chyba – Požaduje po pracovníkovi opravit výdaje, aby byly v souladu se zásadou před odesláním sestavy výdajů nebo cestovní žádanky.       
 
 - Zdůvodnění – Požaduje po pracovníkovi nebo manažerovi zadat odůvodnění částky přesahující zásadu před odesláním sestavy výdajů nebo cestovní žádanky.        

## <a name="policy-tips"></a>Tipy pro zásady
Zde je několik návrhů, které vám mohou pomoci při vytváření nových zásad pro správu výdajů. 
* Zásady mají časovou platnost a neuplatní se, pokud je zásada vytvořena s datem po datu, kdy došlo k výdaji. Vytváříte-li například novou zásadu dnes za účelem vynucení maximálních výdajů na jídlo ve výši 50 USD, nebude možné proti této zásadě kontrolovat existující výdaje, které jste zadali včera.
* Při vytváření zásady pro kategorii výdajů, která může být rozepsaná, zvažte přidání podmínky pro typ řádku výdajů. Některé zásady, jako je například vyžadování účtenky, nemusí mít smysl pro rozepsané řádky a měly by být použity pouze na řádek záhlaví nebo na nerozepsaný řádek. 

## <a name="when-to-evaluate-policies"></a>Kdy vyhodnotit zásady

V parametrech správy výdajů je k dispozici možnost vyhodnotit zásady správy výdajů při uložení řádku nebo při odeslání sestavy výdajů. Rozhodnete-li se vyhodnocovat při uložení řádku, zajistíte, že uživatelé mají včasnější viditelnost toho, co musí udělat pro dokončení všech svých sestav výdajů najednou. V opačném případě můžete zpozdit vyhodnocení zásady a ušetřit čas v případě, že dochází k ověření na konci během odesílání do workflow.
