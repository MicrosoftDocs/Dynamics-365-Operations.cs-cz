---
title: Profily sazeb
description: Toto téma popisuje, jak nastavit data pro profily sazeb.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2512b79c87a4640a2b31b7699e85d743b451a14c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676432"
---
# <a name="rating-profiles"></a>Profily sazeb

[!include [banner](../../includes/banner.md)]

Profil sazby se podobá logistické smlouvě (ale nikoli právní smlouvě). Používá se k určení přepravních tarifů pro náklady. 

Každý profil sazeb je pro dopravce jedinečný. V profilu přidružíte dopravce k hlavní sazbě. Hlavní sazba definuje přiřazení základní sazby a základní sazbu. Základní sazba určuje sazbu dopravce.

Profil sazeb můžete nastavit pomocí obecné stránky, která zobrazuje přehled o všech existujících profilech. Nebo můžete také nastavit profil sazeb přímo od dopravce. V obou případech jsou informace, které jste pro profil hodnocení nastavili, stejné.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Vytvořte nebo upravte profil sazeb na stránce Profily sazeb

Na stránce **Profily sazeb** můžete zkontrolovat všechny dostupné profily sazeb. Můžete také upravit stávající profily a vytvořit nové profily.

1. Přejděte do nabídky **Správa přepravy \> Nastavení \> Sazby \> Profily sazeb**.
1. V podokně akcí vyberte **Nový** pro přidání nového profilu sazeb do mřížky nebo zvolte **Upravit** pro úpravu existujícího profilu.
1. V řádku pro nový nebo stávající profil sazeb nastavte následující pole:

    - **Profil sazeb** – Zadejte jedinečný identifikátor (ID) profilu sazeb.
    - **Název** – Zadejte popisný název profilu sazeb.
    - **Přepravce** - Vyberte přepravce. Profil sazeb, který nastavujete, se také zobrazí na stránce **Přepravci** pro zvoleného přepravce.
    - **Pracoviště** a **Sklad** - Vyberte pracoviště a sklad.
    - **Výpočet přepravních sazeb** - Vyberte výpočet přepravních sazeb pro profil sazeb.
    - **Hlavní sazba** - Vyberte hlavní sazbu pro profil sazeb. Můžete použít základní sazbu k definování základního typu sazby a hlavní sazby. Další informace naleznete v tématu [Nastavení hlavních sazeb](set-up-rate-masters.md).
    - **Modul mezioperačního času** - Vyberte modul mezioperačního času pro profil sazeb.
    - **Index paliva dopravce** - Vyberte index paliva dopravce pro profil hodnocení.
    - **Počáteční datum a čas platnosti** a **Koncové datum a čas platnosti** - Definujte období, kdy by měl být aktivní profil sazeb.

1. V podokně akcí vyberte **Uložit**.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Vytvořte profil sazeb přímo na stránce Přepravci

1. Přejděte do nabídky **Správa přepravy \> Nastavení \> Dopravci \> Dopravci dodávky**.
1. V seznamu vyberte přepravce.
1. Na záložce s náhledem **Profily sazeb** vyberte **Nový** a vytvořte profil sazeb.
1. Nastavte pole pro nový profil sazeb. Tato pole odpovídají polím na stránce **Profily sazeb**, jak je popsáno v předchozí části tohoto tématu.

> [!NOTE]
> Profily, které jsou vytvořeny na stránce **Přepravci**, se také zobrazují na stránce **Profily sazeb**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]