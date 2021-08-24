---
title: Nastavení názvů deníků leasingu
description: Toto téma vysvětluje, jak definovat názvy deníku leasingu. Názvy deníku leasingu určují deníky, do kterých jsou zaúčtovány položky pocházející z leasingu majetku.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7caabeaf92bbce63cc30b2fb76111b33455af1910c2ea822453c550c61e02dd9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740877"
---
# <a name="set-up-lease-journal-names"></a>Nastavení názvů deníků leasingu

[!include [banner](../includes/banner.md)]

Názvy deníku leasingu určují deníky, do kterých jsou zaúčtovány transakce leasingu majetku. Pouze názvy deníků, které jsou přiřazeny typu deníku **Leasing majetku** se objeví v poli **Počáteční uznání** a **Název měsíčního deníku** na stránce **Parametry leasingu majetku**. Pouze typ deníku **záznam faktury dodavatele** lze přiřadit poli **Název deníku faktury**.

Chcete-li nakonfigurovat názvy deníku leasingu, postupujte takto.

1. Přejděte do nabídky **Leasing majetku \> Nastavení \> Parametry leasingu majetku**.
2. Na kartě **Obecné** v poli **Název deníku pro počáteční uznání** vyberte deník. Všechny deníkové položky počátečního uznání budou zaúčtovány k tomuto názvu deníku.
3. V poli **Název deníku faktury** vyberte název deníku. Pokud je možnost **Platba dodavateli** nastavena na **Ano** pro knihu leasingu, budou leasingové faktury a faktury na platbu výdajů zaúčtovány u tohoto názvu deníku.
4. V poli **Název deníku leasingu** vyberte název deníku. Všechny odpisy, úroky a krátkodobé reklasifikační položky budou zaúčtovány pod tímto názvem deníku. Pokud je možnost **Platba dodavateli** nastavena na **Ne** pro knihu leasingu, budou leasingové faktury a faktury na platbu výdajů zaúčtovány u tohoto názvu deníku.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
