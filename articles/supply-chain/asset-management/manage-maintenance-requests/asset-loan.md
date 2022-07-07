---
title: Zapůjčený majetek
description: Tento článek popisuje, jak registrovat zapůjčený majetek v modulu Správa majetku.
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
ms.openlocfilehash: f70b29ef69b80160f108e6f53edda12b86c2c9db
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015747"
---
# <a name="asset-loans"></a>Zapůjčený majetek

[!include [banner](../../includes/banner.md)]

 

Pokud vaše společnost obdrží aktiva pro práce opravy nebo údržby z interních míst nebo od odběratelů a pokud dočasně půjčíte majetek na tato místa nebo těmto zákazníkům, může modul Správa majetku sledovat zapůjčený majetek.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Registrace půjček majetku v požadavku na údržbu

1. Vyberte **Správa majetku** \> **Požadavky na údržbu** \> **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu**.
2. Vyberte požadavek na údržbu, na kterém má být zaregistrován zapůjčený majetek, a pak vyberte možnost **Upravit**.
3. Na stránce **Požadavek** vyberte **Odeslat zapůjčený majetek**.
4. Vyberte majetek a zadejte očekávané datum vrácení.
5. Vyberte **OK**.

> [!NOTE]
> - Zapůjčený majetek lze odeslat pouze v případě, že je k dispozici majetek se stejným typem majetku.
> - Zapůjčený majetek musí mít stav životního cyklu majetku, který umožňuje použití jako investiční majetek, jako je například **InStorage.** Po registraci zapůjčeného majetku se stav životního cyku majetku automaticky aktualizuje například na **OnLoan**.

Chcete-li zobrazit seznam všech majetků, které jste zapůjčili na jiná místa nebo jiným zákazníkům, vyberte možnost **Správa majetku** \> **Zapůjčený majetek** \> **Všechen zapůjčený majetek**. Pokud je u majetku zaškrtnuto políčko **ukončeno**, byl majetek registrován jako vrácený do vaší společnosti.

![Správa požadavků na údržbu.](media/06-manage-maintenance-requests.png)

Na stránce **aktivní zapůjčený majetek** můžete zobrazit seznam všeho zapůjčeného majetku, který nebyl ještě vrácen do vaší společnosti.

## <a name="register-loan-assets-as-returned"></a>Registrace zapůjčeného majetku jako vráceného

1. Vyberte **Správa majetku** \> **Zapůjčený majetek** \> **Aktivní zapůjčený majetek**.
2. Vyberte zapůjčený majetek, který chcete zaregistrovat jako vrácený, a poté vyberte **Vrátit zapůjčený majetek**.
3. V poli **Vráceno** zadejte datum a čas.
4. Vyberte **OK**.
5. Aktualizujte stránku seznamu **Aktivních zapůjčený majetek** a všimněte si, že se zapůjčený majetek již v seznamu nezobrazí.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]