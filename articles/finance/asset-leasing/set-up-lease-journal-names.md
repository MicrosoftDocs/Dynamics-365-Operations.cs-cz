---
title: Nastavení názvů deníků leasingu
description: Tento článek vysvětluje, jak definovat názvy deníku leasingu. Názvy deníku leasingu určují deníky, do kterých jsou zaúčtovány položky pocházející z leasingu majetku.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 678587e0846f6ce6d6d8113290a90b3f4d1988cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874689"
---
# <a name="set-up-lease-journal-names"></a>Nastavení názvů deníků leasingu

[!include [banner](../includes/banner.md)]


Názvy deníku leasingu určují deníky, do kterých jsou zaúčtovány transakce leasingu majetku. Pouze názvy deníků, které jsou přiřazeny typu deníku **Leasing majetku** se objeví v poli **Počáteční uznání** a **Název měsíčního deníku** na stránce **Parametry leasingu majetku**. Pouze typ deníku **záznam faktury dodavatele** lze přiřadit poli **Název deníku faktury**.

Systém zablokuje úpravu určitých finančních polí, aby se zabránilo jakýmkoli odchylkám mezi transakcemi a plány. Mezi zamčená pole patří: **Účet**, **Množství**, **Finanční dimenze**, **Měna** a **Typ transakce**. Kromě toho nebudete moci přidávat ani odstraňovat řádky záznamů deníku v žádných položkách deníku leasingu majektu, protože to může způsobit odchylky mezi plány a transakcemi.


Chcete-li nakonfigurovat názvy deníků leasingu, postupujte takto.

1. Přejděte do nabídky **Leasing majetku \> Nastavení \> Parametry leasingu majetku**.
2. Na kartě **Obecné** v poli **Název deníku pro počáteční uznání** vyberte deník. Všechny deníkové položky počátečního uznání budou zaúčtovány k tomuto názvu deníku.
3. V poli **Název deníku faktury** vyberte název deníku. Pokud je možnost **Platba dodavateli** nastavena na **Ano** pro knihu leasingu, budou leasingové faktury a faktury na platbu výdajů zaúčtovány u tohoto názvu deníku.
4. V poli **Název deníku leasingu** vyberte název deníku. Všechny odpisy, úroky a krátkodobé reklasifikační položky budou zaúčtovány pod tímto názvem deníku. Pokud je možnost **Platba dodavateli** nastavena na **Ne** pro knihu leasingu, budou leasingové faktury a faktury na platbu výdajů zaúčtovány u tohoto názvu deníku.
5. V poli **Název deníku změny leasingu** vyberte deník. Transakce úpravy, ukončení a snížení hodnoty leasingu budou zaúčtovány pod tento název deníku. Název deníku, který vyberete, by neměl mít přiřazen pracovní postup nebo schválení. Pokud není definován název deníku změny leasingu, transakce úpravy, ukončení a snížení hodnoty leasingu budou zaúčtovány pod názvem deníku, který je vybrán v poli **Název deníku leasingu**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
