---
title: Zapůjčený majetek
description: Toto téma popisuje, jak registrovat zapůjčený majetek v modulu Správa majetku.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 712f3e7cdfb8d521ae2afb59d90bc5102da53cb7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813380"
---
# <a name="asset-loans"></a>Zapůjčený majetek

[!include [banner](../../includes/banner.md)]

 

Pokud vaše společnost obdrží aktiva pro práce opravy nebo údržby z interních míst nebo od odběratelů a pokud dočasně půjčíte majetek na tato místa nebo těmto zákazníkům, může modul Správa majetku sledovat zapůjčený majetek.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Registrace půjček majetku v požadavku na údržbu

1. Vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu**.
2. Vyberte požadavek na údržbu, na kterém má být zaregistrován zapůjčený majetek, a pak vyberte možnost **Upravit**.
3. Na stránce **Požadavek** vyberte **Odeslat zapůjčený majetek**.
4. Vyberte majetek a zadejte očekávané datum vrácení.
5. Vyberte **OK**.

> [!NOTE]
> - Zapůjčený majetek lze odeslat pouze v případě, že je k dispozici majetek se stejným typem majetku.
> - Zapůjčený majetek musí mít stav životního cyklu majetku, který umožňuje použití jako investiční majetek, jako je například **InStorage.** Po registraci zapůjčeného majetku se stav životního cyku majetku automaticky aktualizuje například na **OnLoan**.

Chcete-li zobrazit seznam všech majetků, které jste zapůjčili na jiná místa nebo jiným zákazníkům, vyberte možnost **Správa majetku** \> **Společné** \> **Zapůjčený majetek** \> **Všechen zapůjčený majetek**. Pokud je u majetku zaškrtnuto políčko **ukončeno**, byl majetek registrován jako vrácený do vaší společnosti.

![Správa požadavků na údržbu](media/06-manage-maintenance-requests.png)

Na stránce **aktivní zapůjčený majetek** můžete zobrazit seznam všeho zapůjčeného majetku, který nebyl ještě vrácen do vaší společnosti.

## <a name="register-loan-assets-as-returned"></a>Registrace zapůjčeného majetku jako vráceného

1. Vyberte **Správa majetku** \> **Společné** \> **Zapůjčený majetek** \> **Aktivní zapůjčené majetky**.
2. Vyberte zapůjčený majetek, který chcete zaregistrovat jako vrácený, a poté vyberte **Vrátit zapůjčený majetek**.
3. V poli **Vráceno** zadejte datum a čas.
4. Vyberte **OK**.
5. Aktualizujte stránku seznamu **Aktivních zapůjčený majetek** a všimněte si, že se zapůjčený majetek již v seznamu nezobrazí.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]