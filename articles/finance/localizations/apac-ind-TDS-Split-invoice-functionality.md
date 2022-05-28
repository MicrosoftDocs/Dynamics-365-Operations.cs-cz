---
title: Funkce rozdělené faktury
description: Toto téma popisuje nastavení a funkce pro rozdělení faktur podle doručovací adresy a čísla daňového účtu (TAN).
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
ms.openlocfilehash: f1dac8d51c24009dcf0c4acbc49f06f32abf0dec
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724662"
---
# <a name="split-invoice-functionality"></a>Funkce rozdělené faktury

[!include [banner](../includes/banner.md)]

Toto téma popisuje nastavení a funkce pro rozdělení faktur podle doručovací adresy a čísla daňového účtu (TAN).

Na stránce **Parametry závazků** na kartě **Všeobecné** vyberte políčko **Příjem produktu** nebo **Faktura** pro zaúčtování a rozdělení dokladu o produktu nebo faktury, která má na serveru jiné doručovací adresy a čísla TAN na stránce **Nákupní objednávka**. Zaúčtovaná faktura bude poté rozdělena podle doručovací adresy a TAN.

Na kartě **Souhrnná aktualizace** na pevné záložce **Rozdělit na základě** v řádku **Informace o doručení** nastavte možnost **Potvrzení**, **Výdejka**, **Dodací list** nebo **Faktura** na **Ano** k zaúčtování a rozdělení potvrzení, výdejky, dodacího listu nebo faktury, kde jsou pro různé řádky faktury na stránce **Prodejní objednávka** definovány různé řádky faktury. Faktura bude nejprve rozdělena podle doručovací adresy a pak TAN.

> [!IMPORTANT]
> - Pokud nejsou žádné možnosti pro **Informace o doručení** nastaveny na **Ano**, bude faktura zaúčtována jako jedna faktura. K rozdělení faktur nedojde.
> - Chcete-li rozdělit a zaúčtovat dodací list, kde řádky faktury mají různé dodací adresy a TAN, musíte nastavit možnost **Dodací list** pro **Informace o doručení** na **Ano**.
> - Chcete-li rozdělit a zaúčtovat fakturu, kde řádky faktury mají různé dodací adresy a TAN, musíte nastavit možnost **Faktura** pro **Informace o doručení** na **Ano**.
> - Chcete-li rozdělit a zaúčtovat fakturu, kde řádky faktury mají různé dodací adresy, ale stejné TAN, musíte nastavit možnost **Faktura** pro **Informace o doručení** na **Ne**. Faktura bude rozdělena podle doručovací adresy.

## <a name="example"></a>Příklad

V tomto příkladu možnost **Faktura** pro **Informace o doručení** je nastavena na **Ano** na kartě **Souhrnná aktualizace** stránky **Parametry závazků**. Zaúčtuje se nákupní faktura, která má následující nastavení pro doručovací adresy a TAN na řádcích:

- **Řádek položky 1:** Dodací adresa 1, TAN-ABCD12345A
- **Řádek položky 2:** Dodací adresa 1, TAN-ABCD12345A
- **Řádek položky 3:** Dodací adresa 2, TAN-ABCE12345B
- **Řádek položky 4:** Dodací adresa 3, TAN-ABCD12345A

V tomto případě je původní faktura rozdělena na dvě faktury a zaúčtována následujícím způsobem:

- Faktura 1 se zaúčtuje pro řádek 1 položky a řádek 2 položky, protože oba řádky mají stejnou doručovací adresu a TAN.
- Faktura 2 se zaúčtuje za řádek 3 položky.
- Faktura 3 se zaúčtuje za řádek 4 položky.
