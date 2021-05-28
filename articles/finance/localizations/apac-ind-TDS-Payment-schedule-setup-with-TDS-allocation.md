---
title: Nastavení platebního kalendáře s přidělením TDS
description: Toto téma vysvětluje, jak nastavit plány plateb s alokací daně odečtené u zdroje (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023096"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Nastavení platebního kalendáře s přidělením TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit plány plateb s alokací daně odečtené u zdroje (TDS).

1. Přejděte do nabídky **Závazky \> Nastavení platby \> Platební kalendáře**.

    [![Stránka Platební kalendáře](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. V podokně akcí vyberte **Nový** pro vytvoření platebního kalendáře a zadejte požadované údaje.
3. V poli **Přidělení** vyberte metodu, která se použije k alokaci platby pro časový plán plateb:

    - Celkem
    - Pevná částka
    - Fixní množství
    - Určeno

    Pole **Přidělení srážkové daně** zobrazuje metodu přidělení TDS pro plán plateb. Pokud vyberete **Součet** v poli **Přidělení**, pole **Přidělení srážkové daně** je automaticky nastaveno na **Součet**. Pokud vyberete **Pevná částka**, **Pevné množství** nebo **Specifikováno** v poli **Přidělení**, pole **Přidělení srážkové daně** je automaticky nastaveno na **Proporčně**.

    > [!NOTE]
    > Pokud je pole **Přidělení srážkové daně** nastaveno na **Součet**, splátky plateb se počítají na základě hrubé částky, která zahrnuje částku TDS. Pokud je pole **Přidělení srážkové daně** nastaveno na **Proporčně**, splátky plateb se počítají na základě čisté částky faktury po odečtení částky TDS.

4. Zadejte další požadované údaje a poté zavřete stránku.
