---
title: Vytvořte účet úložiště Azure a trezor klíčů
description: Toto téma vysvětluje, jak vytvořit účet úložiště Azure a trezor klíčů.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b8e39539f767cc2944a9a7fdda09121921c64763
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835921"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Vytvořte účet úložiště Azure a trezor klíčů

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Doplňková služba elektronické fakturace přebírá odpovědnost za ukládání všech vašich obchodních údajů v prostředcích Microsoft Azure, které vlastní vaše společnost. Abyste zajistili, že služba funguje správně a že ke všem obchodním datům, která jsou potřebná a generovaná doplňkem elektronické fakturace, přistupuje pouze doplněk, musíte vytvořit dva hlavní zdroje Azure:

- Účet úložiště Azure (úložiště Blob) k ukládání elektronických faktur
- Trezor klíčů Azure k ukládání certifikátů a identifikátoru URI (Uniform Resource Identifier) účtu úložiště

> [!NOTE]
> Vyhrazený zdroj úložiště klíčů a úložiště objektů blob zákazníka musí být přiděleny konkrétně pro použití s doplňkem elektronické fakturace.

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

9. V dialogovém okně **Objekt zabezpečení** vyberte objekt zabezpečení přidáním **Doplněk elektronické fakturace**.
10. Vyberte **Přidat** a potom vyberte **Uložit změny Trezoru klíčů**.
11. Na stránce **Přehled** zkopírujte hodnotu **Název DNS** pro trezor klíčů. Tato hodnota bude použita během instalace služby v RCS a bude označována jako *identifikátor URI trezoru klíčů*.