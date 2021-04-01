---
title: Vytvoření profilu skladového místa
description: Toto téma vysvětluje, jak vytvořit profil skladového místa v aplikaci Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9be25004452ab0a0e2af0ac552a69f805d301d8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239055"
---
# <a name="create-a-location-profile"></a>Vytvoření profilu skladového místa

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit profil skladového místa v aplikaci Dynamics 365 Supply Chain Management. Každé umístění ve skladu musí mít přidružený profil umístění, který popisuje vlastnosti umístění, například zda umístění povoluje smíšené zboží. V této proceduře vytvoříte profil pro umístění, které nevyžaduje kontrolu registrační značky. Povolíme stav Smíšené zboží a Smíšené zásoby a také periodickou inventuru. Tento postup můžete projít v ukázkových datech společnosti USMF.


1. V navigačním podokně přejděte na **Moduly > Řízení skladu > Nastavení > Sklad > Profily skladového místa**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **ID profilu skladového místa**.
4. Zadejte hodnotu do pole **Název**.
5. V poli **Formát skladového místa** zadejte nebo vyberte hodnotu.
6. V poli **Typ skladového místa** zadejte nebo vyberte hodnotu.
7. V poli **ID profilu správy dokování** zadejte nebo vyberte hodnotu.
8. Vyberte možnost **Ano** v poli **Povolit smíšené položky**.
9. Vyberte možnost **Ano** v poli **Povolit smíšené stavy zásob**.
10. Vyberte možnost **Ano** v poli **Povolit cyklickou inventuru**.
11. Zvolte **Uložit**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]