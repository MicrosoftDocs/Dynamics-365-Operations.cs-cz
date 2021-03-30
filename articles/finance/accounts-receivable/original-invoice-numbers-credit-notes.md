---
title: Odkazy na původní faktury v dobropisech
description: Toto téma vysvětluje, jak nastavit a vytisknout původní čísla faktur v souvisejících dobropisech.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 04a4fc96cb7de60052b17e36c33ad5d5be322be4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207344"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Odkazy na původní faktury v dobropisech

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

V některých zemích a regionech existuje zákonný požadavek, aby tištěné dobropisy obsahovaly odkazy na původní faktury. Toto téma vysvětluje, jak nastavit a vytisknout původní čísla faktur v souvisejících dobropisech.

## <a name="prerequisites"></a>Předpoklady

- V pracovním prostoru **Správa funkcí** zapněte funkci **Rozvržení opravné fakturace v sestavách faktur dodavatele**. Další informace naleznete v tématu [Přehled správy funkcí](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).
- Tiskové formáty požadovaných dokumentů musí být nakonfigurovány ve správě tisku.

Funkce popsané v tomto tématu platí pro následující dokumenty:

**Pohledávky**

- Dobropis s volným textem
- Dobropis zákazníkům

**Řízení projektů a účetnictví**

- Dobropis projektu

## <a name="configure-accounts-receivable-parameters"></a>Konfigurujte parametry pohledávek.

Pomocí těchto kroků nastavíte parametr, který řídí, zda se odkazy na původní faktury vytisknou na souvisejících dobropisech.

1. Přejděte do **Pohledávky** \> **Nastavení** \> **Parametry pohledávek**.
2. Na kartě **Aktualizace** na pevné záložce **Faktura** nastavte možnost **Použije rozvržení opravné fakturace v sestavách prodejních faktur a projektů** na **Ano**.

![Konfigurace parametrů pohledávek](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Definujte odkazy na původní faktury

Pomocí následujících postupů definujte odkazy na původní faktury na základě typu dokumentu.

### <a name="free-text-credit-note"></a>Dobropis s volným textem

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Vytvořte nový dobropis nebo vyberte stávající dobropis.
3. Otevřete fakturu.
4. V podokně akcí na kartě **Faktura** ve skupině **Funkce** zvolte **Opravná fakturace**.
5. Zadejte odkaz na původní fakturu a vyberte důvod opravy.

![Definování odkazu na fakturu s volným textem](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Dobropis zákazníkům

1. Přejděte na **Pohledávky** \> **Objednávky** \> **Všechny prodejní objednávky**.
2. Vyberte a otevřete fakturovanou prodejní objednávku, kterou je třeba opravit.
3. V podokně akcí na kartě **Prodej** ve skupině **Dobropis** zvolte **Dobropis**.
4. Zadejte důvod opravy. Odkaz na původní fakturu se vytvoří automaticky.

![Definování odkazu na prodejní objednávku](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Dobropis projektu

1. Přejděte na **Řízení projektu a účetnictví** \> **Faktury projektu** \> **Faktury projektu**.
2. Vyberte a otevřete fakturu projektu, kterou je třeba opravit.
3. V podokně akcí na kartě **Faktura projektu** ve skupině **Funkce** zvolte **Vybrat pro dobropis**.
4. Vyberte **Opravná fakturace**.
5. Zadejte důvod opravy. Odkaz na původní fakturu se vytvoří automaticky.

![Definování odkazu na projektovou fakturu](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Tisk dobropisů

Když vytisknete deobropisy s volným textem, dobropisy zákazníků a projektů, budou obsahovat odkaz na původní fakturu a důvod opravy.

![Vytištěný dobropis](media/credit-note-FTI.jpg)

> [!NOTE]
> Ujistěte se, že jsou tiskové formáty dokumentů správně nakonfigurovány za předpokladu, že budou vytištěny odkazy na původní faktury.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]