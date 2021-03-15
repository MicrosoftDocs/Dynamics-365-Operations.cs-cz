---
title: Proces nastavení rozšířeného odsouhlasení banky
description: Funkce Rozšířené odsouhlasení banky umožňuje importovat elektronické bankovní výpisy a automaticky je odsouhlasit z bankovních transakcí v aplikaci Microsoft Dynamics 365 Finance. Tento článek vysvětluje nastavení procesů odsouhlasení.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: roschlom
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b3c68c8e985e5ef770421cb5e7120db4d97d1de
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976483"
---
# <a name="advanced-bank-reconciliation-setup-process"></a>Proces nastavení rozšířeného odsouhlasení banky

[!include [banner](../includes/banner.md)]

Funkce Rozšířené odsouhlasení banky umožňuje importovat elektronické bankovní výpisy a automaticky je odsouhlasit z bankovních transakcí v aplikaci Microsoft Dynamics 365 Finance. Tento článek vysvětluje nastavení procesů odsouhlasení.  

Existuje několik prvků, které musí být nastaveny před použitím funkce Rozšířené bankovního odsouhlasení. Další informace o nastavení importu bankovního výpisu naleznete v tématu [Nastavení procesu importu rozšířené bankovního odsouhlasení](set-up-advanced-bank-reconciliation-import-process.md).  Požadavky pro nastavení procesu odsouhlasení jsou podrobně popsány níže.

## <a name="transaction-codes"></a>Kódy transakce
Kódy transakcí lze použít jako součást pravidel párování pro odsouhlasení banky. Kódy transakcí vám pomohou spárovat pouze stejné typy transakcí mezi aplikací Finance a vaším bankovním výpisem. Abyste mohli provést tento typ párování, je nutné nejprve definovat typy transakcí pro bankovní transakce z aplikace Finance a potom namapovat tyto typy na kódy transakcí výpisu používané vaší bankou. Typy transakcí pro bankovní transakce jsou definovány na stránce **Typ bankovní transakce**. To je také místo, kde můžete definovat hlavní účet pro účtování přiřazený k tomuto typu transakce. 

Jakmile jsou definovány vaše kódy bankovních transakcí, namapujte je na kódy transakcí používané ve vašich elektronických bankovních výpisech. Tento proces mapování se provádí pomocí stránky **Mapování kódu transakce**. Mapování kódu transakce je dokončeno samostatně pro každý bankovní účet.

## <a name="matching-rules-and-matching-rule-sets"></a>Pravidla spárování a sady pravidel párování
Pravidla párování vám umožňují definovat kritéria pro automatické odsouhlasení mezi bankovními transakcemi aplikací Finance a transakcemi bankovního výpisu. Nastavení pravidel párování se provádí na stránce **Pravidla párování pro odsouhlasen**. Další informace naleznete v tématu [Nastavení sady pravidel párování pro odsouhlasení banky](set-up-bank-reconciliation-matching-rules.md). 

Sady pravidel párování se používají pro definování skupiny pravidel párování, která se spustí v pořadí v průběhu procesu odsouhlasení banky.  Sady pravidel párování jsou konfigurovány na stránce **Sady pravidel párování pro odsouhlasení**.

## <a name="cash-and-bank-management-parameters"></a>Parametry pokladny a banky
Existuje několik parametrů specifických pro proces rozšířeného bankovního odsouhlasení na stránce **Parametry pokladny a banky**.  Možnost **Zobrazit částku řádku výpisu ve formátu Má dáti/Dal** změní zobrazení částek na stránce **Bankovní výpis**. Pokud je vybrána tato možnost, zobrazí se v samostatných sloupcích Má dáti a Dal částky transakce bankovního výpisu. Pokud není vybrána, zobrazí se částky transakce bankovního výpisu v jednom sloupci částky s příslušným znaménkem. 

Možnosti ověřování, které jsou nastaveny na stránce parametrů, přepíší volby nastavené na pravidla párování. Nelze například ručně nebo automaticky spárovat dokumenty nad rámec rozdílu dat nastaveného na stránce parametrů. Zároveň pokud je vybrána možnost **Ověřit mapování typu transakce**, typy transakcí musí být namapovány mezi bankovními transakcemi aplikace Finance a transakcemi bankovního výpisu, aby mohly být transakce párovány ručně nebo automaticky. 

Je také nutné nakonfigurovat potřebné číselné řady na stránce **Parametry pokladny a banky**.  Na kartě **Číselné řady** nastavte kódy číselných řad pro stažení odkazů **ID, ID výpisu, ID odsouhlasení a bankovního odsouhlasení**.

## <a name="bank-account-reconciliation-options"></a>Možnosti odsouhlasení bankovního účtu
Nejdříve musíte povolit rozšířené odsouhlasení banky pro bankovní účet. Jakmile je povolena funkce Rozšířené bankovního odsouhlasení, bude k dispozici na stránce **Bankovní účet** k dispozici několik dalších možností. 

Funkce **Použít bankovní výpisy jako potvrzení elektronické platby** integruje funkci odsouhlasení banky se stavem elektronické platby. Pokud je tato možnost povolena, vytvoří se automaticky bankovní dokument pro elektronické platby se stavem nastaveným na **Odesláno**. Kromě toho se stav elektronické platby aktualizuje z **Odesláno** na **Přijato** poté, co bude platba spárována, odsouhlasena a zaúčtována. 

Pole **Název bankovního účtu v příkazech** představuje název používaný pro bankovní účet ve vašich elektronických bankovních výpisech. Tento název se používá při určování transakcí, které mají být importovány do bankovního účtu z příkazu, který může obsahovat informace pro více bankovních účtů. 

Možnost **Po importu odsouhlasit** automaticky ověří bankovní výpis, vytvoří nové odsouhlasení banky a list a spustí výchozí sadu pravidel párování. Tato funkce automatizuje proces až do okamžiku, kdy musíte odpovídající transakce ručně spárovat. Při importu bude nastaveno výchozí nastavení bankovního účtu





[!INCLUDE[footer-include](../../includes/footer-banner.md)]