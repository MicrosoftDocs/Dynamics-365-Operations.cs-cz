---
title: "Nastavení výdejů v seskupení"
description: "Toto téma popisuje, jak nastavit výdej v seskupení a způsob použití potvrzení položek s výdejem v seskupení."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2ec0890963b2b01407acac8003453faf370894b4
ms.openlocfilehash: 1c23421ddfda8c5f6fa27a31831a00ead6094db9
ms.contentlocale: cs-cz
ms.lasthandoff: 04/11/2018

---

[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a>Nastavení výdejů v seskupení

Toto téma popisuje, jak umožnit zaměstnancům používat mobilní zařízení k seskupování výdejní práce do seskupení, takže mohou vyskladňovat zboží z jednoho místa pro několik pracovních objednávek současně. Tento úkon se nazývá *výdej v seskupení*.

## <a name="about-cluster-picking"></a>O výdeji v seskupení

Po uvolnění pracovních příkazů do skladu, pracovník použije mobilní zařízení k přiřazení objednávek k seskupení. Seskupení bude organizovat výdejní práci pracovníka. Když je pracovní objednávka přiřazena k seskupení, pracovník musí používat výdej v seskupení k provádění práce výdeje pro danou objednávku. Pracovník nemůže použít jinou metodu výdeje. Je-li pracovní objednávka přiřazena seskupení omylem, musí pracovník rozdělit seskupení a znovu jej vytvořit.

V případě potřeby pracovník může předat seskupení jinému pracovníkovi. Tím se změní stav seskupení na Předáno. Používá-li pracovník mobilní zařízení k označení, že je práce výdeje a příjmu dokončena, musí potvrdit dodávku nebo náklad v klientovi aplikace Dynamics 365 for Finance and Operations.

## <a name="set-up-cluster-picking"></a>Nastavení výdejů v seskupení

Chcete-li povolit výdej v seskupení, je nutné nastavit následující:

-   **Profily seskupení** – Určují, zda automaticky generovat ID seskupení, počet pozic, které mají být použity, kdy mají být seskupení rozdělena a jak řadit a ověřovat práci výdeje.

-   **Šablony práce** – Definování způsobu vytváření práce výdeje pro výdej v seskupení.

-   **Směrnice skladového místa** – Určují, odkud zboží vyskladňovat a kam ho dávat.

-   **Položky nabídky mobilního zařízení** – Konfigurace položky nabídky mobilního zařízení pro použití stávající práce, která se řídí výdejem v seskupení. Potom je nutné přidat položku nabídky do nabídky mobilního zařízení tak, aby se zobrazila v mobilním zařízení.

-   **Parametry řízení skladu** – Zadání číselné řady, která se použije, pokud chcete generovat identifikátory pro seskupení.

## <a name="set-up-a-cluster-profile"></a>Nastavení profilu seskupení

Chcete-li nastavit profil seskupení, postupujte následujícím způsobem:

1.  Klikněte na **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Profily seskupení**.

2.  Kliknutím na **Nový** vytvořte nový profil.

3.  Klikněte na tlačítko **Vytvořit seskupení** a pod položkou **Řazení seskupení** klikněte na **Nové** pro nastavení kritérií třídění pro seskupení. Kritéria řazení řídí pořadí, ve kterém bude pracovník provádět práci výdeje. Můžete přidat tolik kritérií, kolik potřebujete.

4.  V poli **Pořadové číslo** zadejte číslo pro definování pořadí, ve kterém se kritéria třídění zpracují.

5.  V poli **Název pole** vyberte pole, které určuje řazení. Vyberete-li například pole **WMSLocationId**, práce bude seřazena podle umístění.

6.  V poli **Třídění** vyberte jednu z následujících možností.

| **Parametr**     | **Popis**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vzestupně**  | Práce výdeje je řazena ve vzestupném pořadí na základě kritérií třídění. Používáte-li například pole **WMSLocationId** jako kritérium třídění a ID skladových míst jsou 1, 2, 3 a 4, výdeje bude nejprve ze skladového místa 4. |
| **Sestupně** | Práce výdeje je řazena v sestupném pořadí na základě kritérií třídění. Používáte-li například pole **WMSLocationId** jako kritérium třídění a ID skladových míst jsou 1, 2, 3 a 4, výdeje bude nejprve ze skladového místa 1. |

## <a name="item-confirmation"></a>Potvrzení položky

Při použití výdeje v seskupení je velmi důležité potvrzení položek k ověření položek, které jsou přidány do seskupení. Při výdeji v seskupení můžete ověřit položky během procesu výdeje v seskupení. Nastavení vychází z nastavení čárového kódu produktu.

### <a name="set-up-item-verification-with-cluster-picking"></a>Nastavení ověření položek s výdejem v seskupení

1.  V položce nabídky mobilního zařízení otevřete formulář nastavení pro potvrzení práce: **Řízení skladu** \> **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Položky nabídky mobilního zařízení**.

2.  Z položky nabídky mobilního zařízení otevřete **Nastavení potvrzení práce**. Možnost **Potvrzení produktu** umožňuje ověřit jednotlivé skladové položky z mobilního zařízení při naskenování.

