---
title: Konfigurace oslovení dodavatele
description: Toto téma popisuje pole, která je třeba vygenerovat v novém oslovení dodavatele.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 987b9cefef395b3bf3e915f41232fe0daba213b9
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021157"
---
# <a name="vendor-request-configurations"></a>Konfigurace oslovení dodavatele
[!include [banner](../includes/banner.md)]

Pro dokončení oslovení dodavatele musí kontaktní osoba dodavatele dokončit průvodce registrace potenciálního dodavatele.

Ve formuláři **Konfigurace oslovení dodavatele**, můžete vytvořit profily určující požadovaná pole a pole viditelná v průvodci registrace potenciálního dodavatele.

Průvodce registrace potenciálního dodavatele se spustí dotazem na uživatele potenciálního dodavatele, ve které zemi/oblasti dodavatel podniká. Tato informace určuje použitelnou konfiguraci. Pokud není žádná konfigurace určena pro zemi nebo oblast, použije se výchozí konfigurace.

### <a name="set-up-a-vendor-request-configuration"></a>Nastavení konfigurace oslovení dodavatele

Ve výchozím nastavení je konfigurace dodavatele k dispozici ve formuláři Konfigurace oslovení dodavatele.

Nelze vybrat země/oblasti pro výchozí konfiguraci, takže nelze změnit část **Země/oblasti**.

1. Klikněte na **Zásobování a zdroje** > **Nastavení** > **Dodavateée** a klikněte na **Konfigurace oslovení dodavatele**.
2. Klikněte na kartu **Pole** pro nastavení stavu uvedených polích.
3. Skryté (není viditelné)
4. Zobrazené (viditelné, ale nepovinné)
5. Požadované (viditelné a povinné)
6. Klikněte na kartu **Obsah** a určete, zda text bude zobrazený v průvodci a zda se má zobrazovat potvrzení o nutnosti přijetí uživatelem potenciálního dodavatele předtím, že se v průvodci přesune na další krok. Potvrzení bude požadováno pro všechny smluvní podmínky, které musí uživatel potvrdit, aby mohl pokračovat.

Lze také zadat potvrzovací zprávu, která se zobrazí po dokončení průvodce, a můžete přidat jeden nebo více dotazníků.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Vytvoření konfigurace dodavatele pro určitou zemi/oblast
1.  Klikněte na **Zásobování a zdroje** > **Nastavení** > **Dodavateée** a klikněte na **Konfigurace oslovení dodavatele**.
2.  Klikněte na tlačítko **Nový** pro vytvoření nové konfigurace a zadejte název konfigurace.
3.  Klikněte na tlačítko **Uložit**.
4.  Otevřete kartu **Země/oblasti** a vyberte zemi nebo oblast, pro kterou má být použita konfigurace.
5.  Dokončete konfiguraci podle následujících pokynů pro výchozí konfiguraci.

