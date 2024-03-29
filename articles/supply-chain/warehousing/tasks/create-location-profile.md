---
title: Vytvoření profilu skladového místa
description: Tento článek vysvětluje, jak vytvořit profil skladového místa v aplikaci Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98537f3ad45d66e348ecd489c60d95ef875e5c07
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875036"
---
# <a name="create-a-location-profile"></a>Vytvoření profilu skladového místa

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak vytvořit profil skladového místa v aplikaci Dynamics 365 Supply Chain Management. Každé umístění ve skladu musí mít přidružený profil umístění, který popisuje vlastnosti umístění, například zda umístění povoluje smíšené zboží. V této proceduře vytvoříte profil pro umístění, které nevyžaduje kontrolu registrační značky. Povolíme stav Smíšené zboží a Smíšené zásoby a také periodickou inventuru. Tento postup můžete projít v ukázkových datech společnosti USMF.


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