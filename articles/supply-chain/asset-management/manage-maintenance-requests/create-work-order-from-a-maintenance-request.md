---
title: Vytvoření pracovních příkazů z požadavků na údržbu
description: Tento článek vysvětluje, jak vytvořit pracovní příkaz z požadavku na údržbu v modulu Správa majetku.
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
ms.openlocfilehash: bb54ec3466086afbd87a023a40e346a6a3464c98
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017167"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Vytvoření pracovních příkazů z požadavků na údržbu

[!include [banner](../../includes/banner.md)]

 


Po vytvoření požadavků na údržbu je lze snadno převést na pracovní příkazy. Tento článek popisuje nejrychlejší způsob, jak pracovat s požadavky na údržbu, aktualizovat několik požadavků na údržbu současně a pak vytvořit pracovní příkaz pro několik požadavků na údržbu současně. Na stránce **aktivní požadavky na údržbu** nebo **Moje požadavky na správu mého funkčního místa** je možné také současně pracovat s jedním požadavkem na údržbu a převést jeden požadavek na údržbu na pracovní příkaz.

> [!NOTE]
> Každý požadavek na údržbu může souviset pouze s jedním pracovním příkazem. Do jednoho pracovního příkazu je však možné zahrnout více požadavků na údržbu, a to i v případě, že požadavky na údržbu mají různý majetek.

1. Vyberte **Správa majetku** \> **Požadavky na údržbu** \> **Všechny požadavky na údržbu**.
2. Před vytvořením pracovní objednávky z požadavků na údržbu je nutné vybrat přinejmenším typ úlohy údržby pro požadavky na údržbu a také variantu typu úlohy údržby a obchod, pokud jsou tyto informace relevantní. V zobrazení mřížky můžete snadno aktualizovat informace o požadavku na údržbu.
3. Jakmile budete připraveni vytvořit pracovní příkaz, vyberte požadavky na údržbu, které mají být do ní zahrnuty.

    - Pokud vyberete několik požadavků na údržbu pro převod do pracovního příkazu, musí být před vytvořením pracovního příkazu nastavena hodnota v poli **Majetek** a **Typ práce údržby**.
    - Pokud vyberete jeden požadavek na údržbu pro převod na pracovní příkaz, je nutné před vytvořením pracovního příkazu nastavit pouze pole **Majetek**. Pokud však vytváříte pracovní příkaz, můžete vybrat typ práce údržby (a související variantu a obchod typu práce údržby, pokud jsou tyto informace relevantní) v dialogovém okně **Vytvořit pracovní příkaz**.

4. Vyberte **Pracovní příkaz**.
5. V dialogovém okně **Vytvořit pracovní příkaz** nastavte pole a poté vyberte **OK**.

    Na panelu zpráv může být zobrazeno upozornění, že byl vytvořen nový pracovní příkaz.

    Pokud navíc vytvoříte pracovní příkaz, který je založený na požadavku na údržbu, bude v případě, že je majetek související s požadavkem na údržbu zahrnut do záruční smlouvy, zobrazí se na panelu zpráv upozornění na záruční smlouvu.

6. Vyberte **Správa majetku** \> **Pracovní příkazy** \> **Všechny pracovní příkazy** a otevřete nový pracovní příkaz.

    ![Otevření nového pracovního příkazu.](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]