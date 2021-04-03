---
title: Vytvořte účet úložiště Azure a trezor klíčů
description: Toto téma vysvětluje, jak vytvořit účet úložiště Azure a trezor klíčů.
author: gionoder
manager: AnnBe
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 14463abe7782d786d286fcc619dee00ce85bb620
ms.sourcegitcommit: 4adc57b0e43d9627dca70762ac941762ec4934e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/22/2021
ms.locfileid: "5479338"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Vytvořte účet úložiště Azure a trezor klíčů

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Předpoklady

Před tím, než budete moci provést kroky v tomto tématu, se musíte ujistit, že jsou dokončeny následující úlohy:

- Vytvoření zdroje úložiště klíčů v Azure. Další informace viz [Informace o Trezoru klíčů Azure](https://docs.microsoft.com/azure/key-vault/general/overview).
- Vytvořte účet úložiště Azure (úložiště blob). Další informace viz [Údržba účtu Azure Storage](https://docs.microsoft.com/azure/storage/blobs/).

## <a name="overview"></a>Přehled

V tomto tématu provedete dva hlavní kroky:

- Nastavte účet úložiště Azure a získejte identifikátor URI účtu úložiště.
- Nastavte trezor klíčů pro uložení URI účtu úložiště.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Nastavte účet úložiště Azure a získejte identifikátor URI účtu úložiště

1. Otevřete účet úložiště, který plánujete použít s doplňkem Elektronická fakturace.
2. Přejděte na **Služba Blob** \> **Kontejnery** a vytvořte nový kontejner.
3. Zadejte název kontejneru a nastavte pole **Úroveň veřejného přístupu** na **Soukromé (bez anonymního přístupu)**.
4. Otevřete kontejner a přejděte na **Nastavení \> Zásady přístupu**.
5. Vyberte **Přidat zásady**, chcete-li přidat uloženou zásadu přístupu.
6. Nastavte pole **Identifikátor** a **Oprávnění** dle potřeby. V poli **Oprávnění** byste měli vybrat všechna oprávnění.

    ![Udělení oprávnění úložiště blob](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Zadejte data zahájení a ukončení platnosti. Doba použitelnosti by měla být v budoucnu.
8. Vyberte **OK** pro uložení zásad a poté uložte změny do kontejneru.
9. Vraťte se do účtu úložiště a otevřete **Průzkumník úložiště (náhled)**.
10. Klikněte pravým tlačítkem na kontejner a poté vyberte **Získejte sdílený přístupový podpis**.
11. V dialogovém okně **Sdílený přístupový podpis** zkopírujte a uložte hodnotu do pole **URI**. Tato hodnota bude použita v dalším postupu a bude označována jako *sdílený přístupový podpis URI*.

    ![Výběr a kopírování hodnoty URI](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Nastavte trezor klíčů pro uložení URI účtu úložiště

1. Otevřete trezor klíčů, který hodláte použít s doplňkem Elektronická fakturace.
2. Přejděte na **Nastavení** \> **Tajné kódy** a potom vyberte **Generovat / importovat** pro vytvoření nového tajného kódu.
3. Na stránce **Vytvořte tajný kód** v poli **Možnosti nahrávání** vyberte **Manuální**.
4. Zadat název tajného kódu. Tento název bude použit během instalace služby v Regulatory Configuration Service (RCS) a bude označován jako *tajný název trezoru klíčů*.
5. V poli **Hodnota** vyberte **URI sdíleného přístupového podpisu** a potom vyberte **Vytvořit**.
6. Nastavte zásady přístupu a udělte doplňku elektronické fakturace správnou úroveň zabezpečeného přístupu k tajnému kódu, který jste vytvořili. Přejděte na **Nastavení \> Zásady přístupu** a vyberte **Přidat zásady přístupu**.
7. Nastavte tajná oprávnění pro operace **Získat** a **Seznam**.

    ![Udělení přístupu ke službě](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Nastavte oprávnění pro operace **Získat** a **Seznam**.

    ![Udělení povolení k certifikátu](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. V poli **Vybrat objekt zabezpečení** vyberte **Není vybrán žádný**.
10. V dialogovém okně **Objekt zabezpečení** vyberte objekt zabezpečení přidáním **Služba elektronické fakturace**.
11. Vyberte **Přidat** a potom vyberte **Uložit změny Trezoru klíčů**.
12. Na stránce **Přehled** zkopírujte hodnotu **Název DNS** pro trezor klíčů. Tato hodnota bude použita během instalace služby v RCS a bude označována jako *identifikátor URI trezoru klíčů*.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

