---
title: Nastavení údajů skupiny TDS, PAN a TAN pro dodavatele a zákazníky
description: Toto téma vysvětluje, jak pro dodavatele a zákazníky nastavit informace o skupině daně stržené u zdroje (TDS), trvalém čísle účtu (PAN) a čísle daňového účtu (TAN).
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
ms.openlocfilehash: b736838f1743a39d1f899f2679a31a2c0fe9a2b31e03b29d22af821314f329c9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745741"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>Nastavení údajů skupiny TDS, PAN a TAN pro dodavatele a zákazníky

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak pro dodavatele a zákazníky nastavit informace o skupině daně stržené u zdroje (TDS), trvalém čísle účtu (PAN) a čísle daňového účtu (TAN).

1. Přejděte na **Závazky \> Dodavatelé \> Všichni dodavatelé** nebo **Pohledávky \> Zákazníci \> Všichni zákazníci**.

    [![Stránka Všichni dodavatelé.](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. V podokně akcí vyberte **Nový** pro vytvoření dodavatele nebo zákazníka a zadejte požadované údaje. Případně vyberte existujícího dodavatele nebo zákazníka.
3. Na pevné záložce **Faktura a dodání** v části **Srážková daň** nastavte možnost **Vypočítat srážkovou daň** na **Ano** k výpočtu srážkové daně, TDS nebo daně vybrané u zdroje (TCS) pro dodavatele nebo zákazníka.
4. TDS pro nákupní fakturu se počítá na základě výchozí skupiny TDS, která je definována pro dodavatele nebo zákazníka. V poli **Skupina TDS** vyberte výchozí skupinu TDS.

    > [!NOTE]
    > Když v seznamu vyberete skupinu TDS v poli **Skupina TDS**, pole **Skupina pro srážkovou daň** a **Skupina TCS** nebudou k dispozici.

5. Na pevné záložce **Daňové údaje** v části **Údaje PAN** v poli **Stav** vyberte stav stálého čísla účtu pro dodavatele nebo zákazníka:

    - **Není dostupný** – Prodejce nebo zákazník nemá PAN.
    - **Přijato** – Prodejce nebo zákazník má PAN.
    - **Požádáno** – Prodejce nebo zákazník požádal o PAN.
    - **Neplatný** – Prodejce nebo zákazník má PAN, ale není platné.

6. Pokud jste vybrali **Přijato** v poli **Stav**, což označuje, že prodejce nebo zákazník má PAN, zadejte PAN do pole **Číslo**. PAN musí obsahovat pět abecedních znaků, poté čtyři číselné znaky a jeden abecední znak. Následuje příklad: **ABCDE1260A**.
7. Pokud jste vybrali **Požádáno** v poli **Stav**, což označuje, že prodejce nebo zákazník požádal o PAN, zadejte referenční číslo do pole **Referenční číslo**.
8. V poli **Povaha posuzovaného** vyberte povahu hodnocené kategorie, do které dodavatel nebo zákazník patří:

    - Společnost
    - HUF
    - Potvrdit
    - Fyzická osoba
    - AOP
    - BOI
    - Obecní úřad
    - Další

    [![Pevná záložka Daňové údaje.](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. V podokně akcí na kartě **Dodavatel** ve skupině **Registrovat** výběrem možnosti **ID registrace** otevřete stránku **Spravovat adresy**.
10. Na stránce **Spravovat adresy** na pevné záložce **Daňové údaje** vyberte možnosti **Přidat** nebo **Upravit** k otevření stránky **Spravovat daňové údaje**, kde můžete udržovat záznam o registraci k dani.
11. Na stránce **Spravovat daňové údaje** na pevné záložce **Srážková daň** do pole **Číslo daňového účtu (TAN)** zadejte TAN. TAN musí obsahovat čtyři abecední znaky, poté pět číselných znaků a jeden abecední znak. Následuje příklad: **AFGH54821T**.
12. Zavřete stránku.
