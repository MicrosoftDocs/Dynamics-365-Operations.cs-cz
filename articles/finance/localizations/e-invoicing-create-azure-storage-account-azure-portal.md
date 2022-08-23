---
title: Vytvoření účtu úložiště Azure na Azure Portal
description: Tento článek vysvětluje, jak vytvořit účet úložiště Azure pro Elektronickou fakturaci.
author: gionoder
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5eca23985c48f4e577bd4567cc2e324df5aa9690
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291629"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Vytvoření účtu úložiště Azure na Azure Portal

[!include [banner](../includes/banner.md)]

Všechny elektronické soubory, které jsou generovány službou Elektronická fakturace nebo přecházejí do služby během zpracování, jsou uloženy ve vašich kontejnerech účtu úložiště Microsoft Azure. Abyste zajistili, že Elektronická fakturace bude mít přístup k těmto kontejnerům, musíte službě elektronické fakturace poskytnout token sdíleného přístupového podpisu (SAS) účtu úložiště. Abyste zajistili bezpečné uložení tokenu, neposkytujte token SAS přímo. Místo toho jej uložte do trezoru klíčů Azure a poskytněte tajný kód Azure Key Vault.

1. Otevřete účet úložiště, který plánujete použít se službou Elektronická fakturace.
2. Přejděte do nabídky **Nastavení** \> **Konfigurace** a ujistěte se, že je parametr **Povolit veřejný přístup k objektu Blob** nastaven na **Povoleno**.
3. Přejděte na **Úložiště dat** \> **Kontejnery** a vytvořte nový kontejner.
4. Zadejte název kontejneru a nastavte pole **Úroveň veřejného přístupu** na **Soukromé (bez anonymního přístupu)**.
5. Otevřete nový kontejner a přejděte na **Nastavení** \> **Zásady přístupu**.
6. Vyberte **Přidat zásady**, chcete-li přidat uloženou zásadu přístupu.
7. Pole **Identifikátor** nastavte podle potřeby.
8. V poli **Oprávnění** vyberte všechna oprávnění.

    ![Všechna oprávnění vybraná v poli Oprávnění v dialogovém okně Přidat zásadu.](media/e-invoicing-azure-1.png)

9. Zadejte počáteční a koncové datum. Koncové datum by mělo být v budoucnu.
10. Vyberte **OK** pro uložení zásad a poté uložte změny do kontejneru.
11. Přejděte na **Nastavení** \> **Tokeny sdíleného přístupu** a nastavte hodnoty pole.
12. Zadejte počáteční a koncové datum. Koncové datum by mělo být v budoucnu.
13. V poli **Oprávnění** vyberte následující oprávnění:

    - Číst
    - Přidat
    - Vytvořit
    - Zapsat
    - Odstranit
    - Seznam

14. Vyberte **Vygenerovat token a URL SAS**.
15. Zkopírujte a uložte hodnotu do pole **Adresa URL URL objektu blob**. Tato hodnota bude použita později v této proceduře a bude označována jako *URI sdíleného přístupového podpisu*.
16. Otevřete trezor klíčů, který hodláte použít s Elektronickou fakturací.
17. Přejděte na **Nastavení** \> **Tajné kódy** a výběrem příkazu **Generovat / importovat** vytvořte nový tajný kód.
18. Na stránce **Vytvořte tajný kód** v poli **Možnosti nahrávání** vyberte **Manuální**.
19. Zadat název tajného kódu. Tento název bude použit během instalace služby v Regulatory Configuration Service (RCS) a bude označován jako *název tajného kódu trezoru klíčů*. Další informace o nastavení RCS najdete v tématu [Nastavení služby Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).
20. V poli **Hodnota** zadejte URI sdíleného přístupového podpisu, kterou jste zkopírovali dříve.
21. Vyberte **Vytvořit**.
