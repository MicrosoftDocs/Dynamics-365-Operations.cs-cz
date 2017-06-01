---
title: "Dobropis u hotovostní slevy"
description: "Toto téma obsahuje informace, které pomohou právnickým osobám v rámci České republiky vytvořit, zaúčtovat a tisknout dobropisy pro hotovostní slevy, které jsou přiřazeny odběratelům."
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters, PrintMgmtSetupUIMain, Reasons
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Operations, Core
ms.custom: 273063
ms.assetid: b7cc2add-88dc-4e15-a537-49f3ebe2e37f
ms.search.region: Czech Republic
ms.author: v-elgolu
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ba5cdea0081725486280c7e04c42d9435ab68909
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="credit-note-on-cash-discount"></a>Dobropis u hotovostní slevy

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace, které pomohou právnickým osobám v rámci České republiky vytvořit, zaúčtovat a tisknout dobropisy pro hotovostní slevy, které jsou přiřazeny odběratelům.

Společnosti v rámci České republiky musí vydávat dobropisy pro hotovostní slevy, které jsou přiřazeny odběratelům. Tyto dobropisy musí obsahovat následující informace:

-   Číslo faktury
-   Daň z přidané hodnoty (DPH) a částka z původního dokumentu.
-   Důvod opravy

<a name="prerequisites"></a>Požadavky
-------------

### <a name="set-up-number-sequences"></a>Nastavit číselné řady

Vytvořte souvislou číselnou řadu pro právnickou osobu. Další informace naleznete v tématu [Přehled číselných řad](/dynamics365/operations/organization-administration/number-sequence-overview). Na stránce **Parametry pohledávek** vyberte číselnou řadu, kterou jste vytvořili pro **prodejní dobropis**. Dále byste nastavte číselnou řadu pro **prodejní doklad dobropisu**. Můžete použít stejnou číselnou řadu, jakou jste použili **prodejní dobropis**.

### <a name="set-up-sales-tax-codes"></a>Nastavit kódy DPH

Další informace naleznete v tématu [Přehled o DPH](../general-ledger/indirect-taxes-overview.md).

### <a name="set-up-report-formats-for-documents"></a>Nastavení formátů sestavy pro dokumenty

1.  Přejděte do nabídky **Pohledávky** \> **Nastavení** \> **Formuláře** \> **Nastavení formuláře**.

2.  Na kartě **Obecné** v části **Nastavit možnosti pro formuláře odběratelů** klikněte na **Správa tisku**.

3.  Ve stromu rozbalte položky **Modul – pohledávky** \> **Dokumenty** \> **Faktura odběratele**. V poli **Název sestavy** zadejte nebo vyberte hodnotu.

4.  Ve stromové struktuře pod uzlem **Faktura odběratele** vyberte **Původní**. V poli **Název sestavy** zadejte nebo vyberte hodnotu.

5.  Ve stromu rozbalte položky **Modul – pohledávky** \> **Dokumenty** \> **Volné faktury**. V poli **Název sestavy** zadejte nebo vyberte hodnotu.

6.  Ve stromové struktuře pod uzlem **Volná faktura** vyberte **Původní**. V poli **Název sestavy** zadejte nebo vyberte hodnotu.

### <a name="set-up-customer-reason-codes"></a>Nastavte kódy důvodů odběratele.

Na stránce **Kódy důvodů odběratele** (**Pohledávky** \> **Nastavení** \> **Kódy důvodů odběratele**) vytvořte nebo upravte kódy důvodů, které se používají pro opravné daňové doklady.

### <a name="set-up-accounts-receivable-parameters"></a>Nastavení parametrů pohledávek

Na stránce **Parametry pohledávek** (**Pohledávky** \> **Nastavení** \> **Parametry pohledávek**) na kartě **Vyrovnání** na pevné záložce **Možnosti** nastavte následující parametry:

-   Zaškrtněte políčko **Vyžadovat kódy důvodu pro dobropisy**.

-   Zaškrtněte políčko **Zaúčtovat dobropis pro platební slevu**.

V poli **Kód důvodu pro platební slevy** vyberte výchozí kód důvodu pro opravné daňové doklady.

## <a name="credit-notes-for-cash-discounts"></a>Dobropisy pro platební slevy

Dobropisy pro hotovostní slevy se automaticky zaúčtují při vyrovnání otevřených transakcí odběratele (faktury odběratele a platbu odběratele). Při zaúčtování dobropisů pro hotovostní slevy jsou zahrnuty kódy důvodů, které nastavíte v parametrech pohledávek, a odkaz na původní fakturu.
Dobropisy pro platební slevy jsou číslovány podle číselné řady nastavené pro dobropisy. Výtisk dokumentu je nazván **Opravný dokument daně**. Obsahuje původní číslo faktury, základ a částku DPH a důvod, proč byla vytištěna oprava.


