---
title: Odstraňování potíží se sestavením nákladu a dodávkami
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími se setavením a dodávkami nákladu v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2933bcfd2cc526e39a4e1343cd472334a5b95607
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645325"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Odstraňování potíží se sestavením nákladu a dodávkami

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími se setavením a dodávkami nákladu v Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Zobrazuje se následující chybová zpráva: „Nelze vytvořit řádek nákladu pro tento řádek objednávky, protože obsahuje neplatné dimenze inventáře ...“

### <a name="issue-description"></a>Popis problému

Při pokusu o uvolnění objednávky prodejní vratky do skladu se zobrazí následující chybová zpráva:

> Nelze vytvořit řádek nákladu pro tento řádek objednávky, protože obsahuje neplatné dimenze inventáře. V hierarchii rezervací nemůžete odkazovat na dimenze zásob, které se nacházejí pod dimenzí umístění. Odeberte neplatné rozměry z řádku objednávky.

### <a name="issue-resolution"></a>Řešení problému

Produkt bohužel nepodporuje zpracování nákladu pro proces vrácení prodeje. Proto nemůžete uvolnit objednávku prodejní vratky do skladu.

V transakcích prodejní objednávky nemůžete odkazovat na dimenze zásob, které se nacházejí pod dimenzí **umístění** v hierarchii rezervací. Řešením je odebrání neplatných rozměrů z řádku objednávky.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Zobrazuje se následující chybová zpráva: „Jeden z řádků je již na nákladu. Nelze uvolnit do skladu."

### <a name="issue-description"></a>Popis problému

Pokud ručně vytvoříte náklady nebo nastavíte proces tak, aby se náklady již vytvořily před zadáním řádku prodejní objednávky, předpokládá se, že následné vydání bude provedeno ručně a že bude použita cesta a hodnocení z nákladu.

V jiném možném scénáři se pokoušíte provést automatické uvolnění do skladu, ale vlnovému procesu se nepodařilo vytvořit práci. Proto je stále vytvořena otevřená zásilka nebo náklad. Tato otevřená zásilka nebo náklad poté blokuje následné pokusy o automatické uvolnění objednávky, dokud otevřenou zásilku nebo náklad nezrušíte nebo ručně nezpracujete vlnu.

### <a name="issue-resolution"></a>Řešení problému

Můžete uvolnit ze stránky prodejní objednávky nebo automatické uvolnění lze provést ze stránky prodejní objednávky, pouze pokud před vydáním do skladu neexistuje žádný náklad. Po zpracování vlny se náklad automaticky vytvoří.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Zobrazuje se následující chybová zpráva: „Opravu poznámky k dodání nelze zpracovat. Poznámka k dodání obsahuje pouze položky, které podléhají procesům správy skladu, protože tyto nejsou opravou poznámky k dodání podporovány. "

### <a name="issue-description"></a>Popis problému

Po vystavení poznámky k dodání ji nemůžete zrušit, protože tlačítko **Zrušení** není k dispozici. Poznámku k dodání také nemůžete opravit. Pokud se pokusíte, zobrazí se tato chybová zpráva.

### <a name="issue-resolution"></a>Řešení problému

Chcete-li opravit odeslané dodací listy pro položky, které jsou povoleny pro pokročilou správu skladu (WMS), musíte zaúčtování provést z nákladu, nikoli přímo z objednávky.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Jak mohu vytvořit práci z odchozích nákladů namísto vln?

### <a name="issue-description"></a>Popis problému

Zde je jeden způsob, jak tento problém reprodukovat.

1. Vytvoření odchozího nákladu pomocí prodejní objednávky nebo převodního příkazu.
2. Uvolnit vytížení do skladu
3. Všimněte si, že zatím nebyla vygenerována žádná práce výdeje.

### <a name="issue-resolution"></a>Řešení problému

Pokud musí být práce generována okamžitě po uvolnění nákladu, musíte odpovídajícím způsobem nakonfigurovat šablonu vln. Na šabloně vlny nastavte následující možnosti na *Ano*:

- Automatizovat vytvoření vlny
- Zpracovat vlnu při uvolnění do skladu
- Automatizovat uvolnění vlny

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Částečně odeslaný náklad nemohu znovu uvolnit.

### <a name="issue-description"></a>Popis problému

Částečně odeslaný náklad nemůžete uvolnit do skladu. Když provedete uvolnění do skladu, zobrazí se zpráva „Operace dokončena“, ale nic se nestane a pro zbývající množství se nevytvoří žádná práce. K tomuto problému dochází, když použijete funkci transportu nákladu a dojde k neúplné rezervaci.

### <a name="issue-resolution"></a>Řešení problému

[Problém KB 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Částečně odeslané náklady lze znovu zařadit do vlny a zpracovat“) je opraven [vydaná verze 10.0.15](../get-started/whats-new-scm-10-0-15.md).
