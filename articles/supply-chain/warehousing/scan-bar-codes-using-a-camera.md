---
title: Skenování čárových kódů pomocí fotoaparátu v mobilní aplikaci Řízení skladu
description: Toto téma vysvětluje, jak nastavit mobilní aplikaci Řízení skladu pro skenování čárových kódů pomocí fotoaparátu na mobilním zařízení.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 62280b8401c1f7d5dc859a2130981405e69d03cfb5383123d7069e71e6cb1f47
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711656"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Skenování čárových kódů pomocí fotoaparátu v mobilní aplikaci Řízení skladu

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit mobilní aplikaci Řízení skladu pro skenování čárových kódů pomocí fotoaparátu na mobilním zařízení.

## <a name="setup"></a>Nastavení

V nastavení zobrazení mobilní aplikace Řízení skladu můžete vybrat, zda má být použit fotoaparát ke skenování čárových kódů. Pokud povolíte možnost **Použít fotoaparát jako skener**, lze použít fotoaparát pro každé pole pro zadávání s upřednostňovaným vstupním režimem nastaveným na **Skenování**.

K určení, zda vstupní pole má být skenovatelné, nastavte na stránce **Názvy polí aplikace Sklady** v **Upřednostňovaný režim vstupu** na **Skenování**. Pokud je vybrána tato možnost, fotoaparát slouží pro skenování v mobilní aplikaci Řízení skladu. Další informace viz [Konfigurace polí pro mobilní aplikaci Řízení skladu](configure-app-field-names-priorities-warehouse.md).

## <a name="supported-bar-code-formats"></a>Podporované formáty čárového kódu

Jsou podporovány nejběžnější formáty čárového kódu, včetně kódu 128, kódu 39, kódu 93, EAN-8, EAN-13, UPC-E, UPC-A a QR kódů

## <a name="navigation"></a>Navigace

Stránka fotoaparátu bude spuštěna na každé stránce, kde má vstupní pole **preferovaný vstupní režim** nastavený na *Skenování*. Když se nacházíte na stránce fotoaparátu, použijte pro navigaci následující možnosti:

- Vyberte tlačítko Zpět pro návrat na stránku **úloh a podrobností**.
- Vyberte ikonu tužky na stránce **úloh a podrobností** a přejděte na stránku, kde můžete zadávat vstup ručně.
- Vyberte ikonu fotoaparátu na stránce **úloh a podrobností** pro návrat na stránku fotoaparátu.

Na stránce fotoaparátu po výběru tlačítka fotoaparátu bude toto tlačítko šedé při pokusu o identifikaci čárového kódu. Pokud čárový kód není identifikován do 5 sekund, proces vyprší a tlačítko fotoaparátu bude opět dostupné. Budete pak moci se pokusit znovu o naskenování čárového kódu.

Jestliže zaměříte fotoaparátu na čárový kód, udržujte čárový kód zarovnaný mezi čarami pro dosažení nejlepších výsledků. Při úspěšném naskenování čárového kódu bude zpracován výsledek a budete navedeni k dalšímu kroku. Pokud další krok obsahuje jiné vstupní pole s upřednostňovaným vstupním režimem nastaveným na Skenování, stránka fotoaparátu se znovu spustí. Pokud není dalším krokem skenovací pole, stránka kamery se nespustí.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]