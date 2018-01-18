---
title: "Systémové seskupení na otevřeném seznamu úkolů"
description: "Toto téma popisuje, jak filtrovat seznam otevřené práce u mobilního zařízení."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6403fea54be4036f7a15c05b46f70d258d97c3e2
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="system-grouping-on-an-open-work-list"></a>Systémové seskupení na otevřeném seznamu úkolů

[!include[banner](../includes/banner.md)]

Pomocí pole seskupení systému můžete filtrovat seznam otevřené práci bez nutnosti upravovat položku nabídky mobilního zařízení.
V příslušných případech funguje seskupování systému k filtrování pracovního seznamu u jednoho pole záhlaví práce. Systémové seskupení nelze použít k filtrování na úrovni polí řádku.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Nastavení systémového seskupení v otevřeném seznamu úkolů
Tyto kroky slouží k nastavení systémového seskupení v otevřeném seznamu úkolů.

-   Z položky nabídky mobilního zařízení vyberte **Režim: Nepřímý** a **Kód aktivity: Zobrazit otevřený pracovní seznam**. K dispozici jsou následující možnosti. Tyto možnosti jsou požadovány pro systémové seskupení v otevřeném pracovním seznamu. 

| Parametr        | popis   | 
| ------------- | ------------- |
| Povolit seskupení systému   | Umožňuje seskupení systému pro vybranou položku pracovního seznamu.| 
| Pole systémového seskupení   | K dispozici pouze v případě, že je možnost **Povolit systémovou práci** nastavena na hodnotu **Ano**. Vyberte pole, které určuje způsob seskupení práce pro pracovníky. Pokud například vyberete pole **ShipmentId**, pracovník naskenuje ID dodávky pro seskupení práce výdeje. Všechna práce pro dodávku bude přiřazena pracovníkovi. Toto pole vyžaduje, abyste vytvořili položku nabídky pro stávající práci, která je seskupena podle systému. Pole **Popisek systémového seskupení** použijte k informování pracovníka, co kontrolovat. |
| Popisek systémového seskupení   | K dispozici pouze v případě, že je možnost **Povolit systémovou práci** nastavena na hodnotu **Ano**. Zadejte informace pro pracovníka o tom, co kontrolovat při seskupení práce vyskladnění v aplikaci . Používáte-li například pole **ShipmentId** pro seskupení práce výdeje podle dodávky, měli byste do pole zadat ID dodávky. Toto pole vyžaduje, abyste vytvořili položku nabídky pro stávající práci, která je seskupena podle systému. Je nutné zaškrtnout pole definující seskupení v poli **systémové seskupení**.|

