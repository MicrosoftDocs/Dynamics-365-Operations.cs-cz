---
title: Nastavení zdrojů Azure pro elektronickou fakturaci
description: Tento článek poskytuje přehled procesu nastavení zdrojů Microsoft Azure pro elektronickou fakturaci.
author: gionoder
ms.date: 01/26/2022
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
ms.openlocfilehash: f11e4eac831d54a6cac765a5adc4e4ffddbe0a22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283078"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Nastavení zdrojů Azure pro elektronickou fakturaci

[!include [banner](../includes/banner.md)]

Proces nastavení zdrojů Microsoft Azure pro elektronickou fakturaci má tři kroky. První dva kroky, „Vytvoření Azure Key Vault v Azure Portal“ a „Vytvoření účtu Azure Storage v Azure Portal“, jsou povinné. Třetí krok, „Konfigurace připojení SharePoint,“ je volitelná.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Vytvoření Azure Key Vault na Azure Portal

Vytvořte trezor klíčů v předplatném Azure. Doporučujeme vytvořit samostatný trezor klíčů pro elektronickou fakturaci a nekombinovat tajné klíče s jinými aplikacemi. Vytvořte tolik tajných klíčů a certifikátů, kolik potřebujete pro své scénáře v elektronických dokumentech. Musíte vytvořit alespoň jeden tajný klíč pro uložení tokenu sdíleného přístupového podpisu (SAS) účtu úložiště Azure, který vytvoříte v dalším kroku.

Informace o provedení tohoto kroku naleznete v části [Vytvoření Azure Key Vault na portálu Azure](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Vytvoření účtu úložiště Azure na Azure Portal

Vlastníte všechny elektronické dokumenty a soubory, které služba Elektronická fakturace generuje nebo do služby vstupuje. Tyto dokumenty a soubory jsou uloženy v účtu úložiště Azure, který vytvoříte ve svém předplatném Azure. Služba bude přistupovat k vašemu účtu úložiště pomocí tokenu SAS, který je převzat z vašeho tajného klíče trezoru klíčů.

Informace o provedení tohoto kroku naleznete v části [Vytvoření účtu úložiště Azure na portálu Azure](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>Konfigurace připojení SharePoint

V některých scénářích může být nutné uložit elektronické soubory do SharePoint a získat je z SharePoint. Abyste zajistili, že služba Elektronická fakturace bude mít přístup k vašim složkám SharePoint, nakonfigurujte přístup k SharePoint.

Informace o provedení tohoto kroku naleznete v části [Konfigurace připojení SharePoint](e-invoicing-create-sharepoint-connection.md).
