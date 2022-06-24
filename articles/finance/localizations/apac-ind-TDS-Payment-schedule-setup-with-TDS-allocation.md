---
title: Nastavení platebního kalendáře s přidělením TDS
description: Tento článek vysvětluje, jak nastavit plány plateb s alokací daně odečtené u zdroje (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 48891c32f39b743ce26e265c5682dab28ecb4b27
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868305"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Nastavení platebního kalendáře s přidělením TDS

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak nastavit plány plateb s alokací daně odečtené u zdroje (TDS).

1. Přejděte do nabídky **Závazky \> Nastavení platby \> Platební kalendáře**.

    [![Stránka Platební kalendáře.](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

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
