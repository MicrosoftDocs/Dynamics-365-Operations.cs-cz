---
title: Odkazy na původní faktury v dobropisech
description: Tento článek vysvětluje, jak nastavit a vytisknout původní čísla faktur v souvisejících dobropisech.
author: mrolecki
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: f1f9ca3914aa02cc38ddfe9f8dd88eb7fc88fd4b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281228"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Odkazy na původní faktury v dobropisech

[!include [banner](../includes/banner.md)]


V některých zemích a regionech existuje zákonný požadavek, aby tištěné dobropisy obsahovaly odkazy na původní faktury. Tento článek vysvětluje, jak nastavit a vytisknout původní čísla faktur v souvisejících dobropisech.

## <a name="prerequisites"></a>Předpoklady

- V pracovním prostoru **Správa funkcí** zapněte funkci **Rozvržení opravné fakturace v sestavách faktur dodavatele**. Další informace naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Tiskové formáty požadovaných dokumentů musí být nakonfigurovány ve správě tisku.

Funkce popsané v tomto článku platí pro následující dokumenty:

**Pohledávky**

- Dobropis s volným textem
- Dobropis zákazníkům

**Řízení projektů a účetnictví**

- Dobropis projektu

## <a name="configure-accounts-receivable-parameters"></a>Konfigurujte parametry pohledávek.

Pomocí těchto kroků nastavíte parametr, který řídí, zda se odkazy na původní faktury vytisknou na souvisejících dobropisech.

1. Přejděte do **Pohledávky** \> **Nastavení** \> **Parametry pohledávek**.
2. Na kartě **Aktualizace** na pevné záložce **Faktura** nastavte možnost **Použije rozvržení opravné fakturace v sestavách prodejních faktur a projektů** na **Ano**.

![Konfigurace parametrů pohledávek.](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Definujte odkazy na původní faktury

Pomocí následujících postupů definujte odkazy na původní faktury na základě typu dokumentu.

### <a name="free-text-credit-note"></a>Dobropis s volným textem

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Vytvořte nový dobropis nebo vyberte stávající dobropis.
3. Otevřete fakturu.
4. V podokně akcí na kartě **Faktura** ve skupině **Funkce** zvolte **Opravná fakturace**.
5. Zadejte odkaz na původní fakturu a vyberte důvod opravy.

![Definování odkazu na fakturu s volným textem.](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Dobropis zákazníkům

1. Přejděte na **Pohledávky** \> **Objednávky** \> **Všechny prodejní objednávky**.
2. Vyberte a otevřete fakturovanou prodejní objednávku, kterou je třeba opravit.
3. V podokně akcí na kartě **Prodej** ve skupině **Dobropis** zvolte **Dobropis**.
4. Zadejte důvod opravy. Odkaz na původní fakturu se vytvoří automaticky.

![Definování odkazu na prodejní objednávku.](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Dobropis projektu

1. Přejděte na **Řízení projektu a účetnictví** \> **Faktury projektu** \> **Faktury projektu**.
2. Vyberte a otevřete fakturu projektu, kterou je třeba opravit.
3. V podokně akcí na kartě **Faktura projektu** ve skupině **Funkce** zvolte **Vybrat pro dobropis**.
4. Vyberte **Opravná fakturace**.
5. Zadejte důvod opravy. Odkaz na původní fakturu se vytvoří automaticky.

![Definování odkazu na projektovou fakturu.](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Tisk dobropisů

Když vytisknete deobropisy s volným textem, dobropisy zákazníků a projektů, budou obsahovat odkaz na původní fakturu a důvod opravy.

![Vytištěný dobropis.](media/credit-note-FTI.jpg)

> [!NOTE]
> Ujistěte se, že jsou tiskové formáty dokumentů správně nakonfigurovány za předpokladu, že budou vytištěny odkazy na původní faktury.

## <a name="references-to-original-invoices-in-debit-notes"></a>Odkazy na původní faktury v dluhopisech

Ve výchozím nastavení lze do dobropisů zadat odkazy na původní faktury. Můžete například zadat reference, když provádíte negativní (sestupné) opravy původních faktur.

Chcete-li zadat reference, když provádíte kladné (narůstající) opravy původních faktur, musíte povolit funkci **Odkazy na původní faktury v vrubopisech** v pracovním prostoru **Správa funkcí**.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
