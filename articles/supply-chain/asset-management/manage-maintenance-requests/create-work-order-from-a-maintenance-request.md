---
title: Vytvoření pracovních příkazů z požadavků na údržbu
description: Toto téma vysvětluje, jak vytvořit pracovní příkaz z požadavku na údržbu v modulu Správa majetku.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bc2422e395239560be580ec9dd1335d93b20aadc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354874"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Vytvoření pracovních příkazů z požadavků na údržbu

[!include [banner](../../includes/banner.md)]

 


Po vytvoření požadavků na údržbu je lze snadno převést na pracovní příkazy. Toto téma popisuje nejrychlejší způsob, jak pracovat s požadavky na údržbu, aktualizovat několik požadavků na údržbu současně a pak vytvořit pracovní příkaz pro několik požadavků na údržbu současně. Na stránce **aktivní požadavky na údržbu** nebo **Moje požadavky na správu mého funkčního místa** je možné také současně pracovat s jedním požadavkem na údržbu a převést jeden požadavek na údržbu na pracovní příkaz.

> [!NOTE]
> Každý požadavek na údržbu může souviset pouze s jedním pracovním příkazem. Do jednoho pracovního příkazu je však možné zahrnout více požadavků na údržbu, a to i v případě, že požadavky na údržbu mají různý majetek.

1. Vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Všechny požadavky na údržbu**.
2. Před vytvořením pracovní objednávky z požadavků na údržbu je nutné vybrat přinejmenším typ úlohy údržby pro požadavky na údržbu a také variantu typu úlohy údržby a obchod, pokud jsou tyto informace relevantní. V zobrazení mřížky můžete snadno aktualizovat informace o požadavku na údržbu.
3. Jakmile budete připraveni vytvořit pracovní příkaz, vyberte požadavky na údržbu, které mají být do ní zahrnuty.

    - Pokud vyberete několik požadavků na údržbu pro převod do pracovního příkazu, musí být před vytvořením pracovního příkazu nastavena hodnota v poli **Majetek** a **Typ práce údržby**.
    - Pokud vyberete jeden požadavek na údržbu pro převod na pracovní příkaz, je nutné před vytvořením pracovního příkazu nastavit pouze pole **Majetek**. Pokud však vytváříte pracovní příkaz, můžete vybrat typ práce údržby (a související variantu a obchod typu práce údržby, pokud jsou tyto informace relevantní) v dialogovém okně **Vytvořit pracovní příkaz**.

4. Vyberte **Pracovní příkaz**.
5. V dialogovém okně **Vytvořit pracovní příkaz** nastavte pole a poté vyberte **OK**.

    Na panelu zpráv může být zobrazeno upozornění, že byl vytvořen nový pracovní příkaz.

    Pokud navíc vytvoříte pracovní příkaz, který je založený na požadavku na údržbu, bude v případě, že je majetek související s požadavkem na údržbu zahrnut do záruční smlouvy, zobrazí se na panelu zpráv upozornění na záruční smlouvu.

6. Vyberte **Správa majetku** \> **Společné** \> **Pracovní příkazy** \> **Všechny pracovní příkazy** a otevřete nový pracovní příkaz.

    ![Otevření nového pracovního příkazu.](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]