---
title: Parametry správy rabatu
description: Tento článek popisuje stránku parametrů správy rabatu. Tato stránka obsahuje nastavení, která ovlivňují účtování, aktualizace stavu, číselné řady a další chování.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 218c54d97f3ac204e8613f5efdda0cc9d713ee04
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895518"
---
# <a name="rebate-management-parameters"></a>Parametry správy rabatu

[!include [banner](../includes/banner.md)]

Stránka **Parametry správy rabatu** se používá k definování nastavení, která platí v celém modulu **Správa rabatů**. Tato nastavení ovlivňují účtování, aktualizace stavu, číselné řady a další chování. Nastavení na této stránce je sdíleno mezi právnickými osobami a může být upravováno uživateli, kteří mají příslušná bezpečnostní oprávnění.

Chcete-li otevřít stránku **Parametry správy rabatu**, přejděte na **Správa rabatu \> Nastavení \> Parametry správy rabatu**. Poté nastavte pole, jak je popsáno v následujících pododdílech.

## <a name="rebate-management-tab"></a>Karta správy rabatů

Následující tabulka popisuje pole, která jsou k dispozici na kartě **Správa rabatů** na stránce **Parametry správy rabatů**.

| Pole | popis |
|---|---|
| Výchozí stav | Vyberte výchozí stav pro všechny nové nabídky. Chcete-li definovat sadu hodnot stavu, které jsou k dispozici pro výběr, použijte [stránku **Stavy rabatů**](rebate-statuses.md). |
| Zpracování podle dimenze | Vyberte, zda mají být transakce dodávek, rabatů a odpisů zpracovány podle finanční dimenze. Když je tato možnost zapnutá, systém použije finanční dimenze ze zdrojových transakcí v cílových transakcí. |
| Kontrola dřívějšího zaúčtování | <p>Vyberte chování systému, pokud jsou nazaúčtované transakce rabatů zpracovávány vícekrát za stejné období:</p><ul><li>**Varování** - Systém umožňuje uživatelům přepsat původní řádky transakcí, ale zobrazí se varování.</li><li>**Chyba** - Systém zabraňuje uživatelům přepsat původní řádky transakcí a zobrazí se chybová zpráva. |
| Automatické zaúčtování deníků | Vyberte, zda má systém automaticky zaúčtovat navrhované deníky. Mezi tyto deníky patří denní deníky, které se používají pro dodávky a odpočty zákazníků, a také deníky daňových faktur dodavatele. |
| Automatické zaúčtování volných faktur | Vyberte, zda má systém automaticky zaúčtovat volné faktury. Tato možnost se vztahuje pouze na volné faktury, kde je nastaven typ platby *Odpočty zákazníků daňové faktury*. |
| Odkaz na objednávku položky rabatu | Vyberte odkaz na rabat, který se má použít na prodejních a nákupních objednávkách, které jsou generovány z procesu rabatu (*Žádný*, *Nabídka správy rabatu*, *Číslo správy rabatu*, *Číslo transakce rabatu* nebo *Poznámky k dokumentu*). |
| Použití procesu nároků | <p>Tuto možnost nastavte na *Ano*, chcete-li použít proces nároku. Tímto způsobem můžete označit transakce, které správa rabatu vytvoří, buď jako nárokované nebo nenárokované, a poté zaúčtovat pouze nárokované transakce.</p><p>Například vypočítáte rabaty za měsíční transakce, ale zákazník ponechal dva dny nenárokované. V tomto případě budou nneárokované transakce znovu vytvořeny při příštím spuštění funkce *Zpracovat* pro příští období.</p><p>Pokud nastavíte tuto možnost na *Ne*, jsou zaúčtovány všechny transakce nároků.</p> |
| Zahrnutí deníku typu objednávky | Pro nabídky nebo řádky nabídek, kde je nastaven typ transakce je *Objednávka*, tato volba určuje, zda má prodejní objednávka typu *Deník* být zahrnuta. Poskytuje flexibilitu, pokud se tyto typy objednávek používají ve scénářích, kdy by se ještě neměl uplatnit rabat. |

## <a name="number-sequences-tab"></a>Karta Číselné řady

Použijte kartu **Číselné řady** na stránce **Parametry správy rabatu** pro přiřazení kódů číselných řad různým číselným řadám, které používá správa rabatu. Následující tabulka popisuje účel každé z těchto číselných řad. Další informace o číselných řadách najdete v části [Přehled číselných řad](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) a souvisejících článcích.

| Reference | Popis |
|---|---|
| Obchod správy rabatu | Číselná řada přiřadí každé nabídce rabatu jedinečnou hodnotu klíče. Tento klíč se používá při vytváření nabídek. |
| Číslo správy rabatu | Číselná řada přiřadí každému rabatu jedinečnou hodnotu klíče. Tento klíč se používá k identifikaci vztahů rabatů. |
| Číslo transakce rabatu | Číselná řada přiřadí každé transakci rabatu jedinečnou hodnotu klíče. Tento klíč se používá k identifikaci transakcí rabatů. |
| Daňová faktura | Číselná řada přiřadí každé faktuře rabatu jedinečnou hodnotu klíče. Tento klíč se používá při automatickém zaúčtování deníků rabatů. |

## <a name="feature-visibility-tab"></a>Karta viditelnosti prvku

Správa rabatů přidávají funkce (pole a funkce) do několika často používaných stránek v Microsoft Dynamics 365 Supply Chain Management. Tyto stránky zahrnují stránky, které souvisejí s prodejními objednávkami a prodejními nabídkami. Pokud používáte správu rabatů, musíte tyto funkce zviditelnit všude, než je budete moci používat. Pokud nepoužíváte správu rabatů, můžete funkce skrýt, abyste je nebylo možné používat.

Na kartě **Viditelnost prvku** na stránce **Parametry správy rabatů** nastavte možnost **Aktivovat** na *Ano*, aby funkce správy rabatů byly viditelné všude tam, kde jsou k dispozici. Nastavením této možnosti na *Ne* skryjete funkce na běžných stránkách mimo modul **správy rabatů**. I když je však tato možnost nastavena na *Ne*, samotný modul, včetně stránky **Parametry správy rabatů**, zůstane k dispozici uživatelům, kteří mají příslušná oprávnění k přístupu.
