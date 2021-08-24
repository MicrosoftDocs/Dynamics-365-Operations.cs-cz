---
title: Vytvoření nové funkce elektronické fakturace
description: Toto téma vysvětluje, jak vytvořit novou funkci elektronické fakturace, když pro vaši zemi nebo oblast není k dispozici žádná integrovaná konfigurovatelná funkce.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744928"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Vytvoření nové funkce elektronické fakturace

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit novou funkci elektronické fakturace, když pro vaši zemi nebo oblast není k dispozici žádná integrovaná konfigurovatelná funkce.

K dokončení nové funkce elektronické fakturace dokončete tyto úkoly:

1. Vytvořte novou konfiguraci formátu souboru pomocí poskytnuté konfigurace modelu fakturace a využívejte výhod existujícího mapování faktur pro funkci, kterou chcete vytvořit.
2. Přidejte konfigurace formátu souboru do konfigurací funkcí elektronické fakturace.
3. Vytvořte nastavení funkce elektronické fakturace.
4. Dokončete novou funkci elektronické fakturace a publikujte ji v globálním úložišti pro svou organizaci.
5. Nasaďte novou funkci elektronické fakturace do prostředí služby.

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Vytvoření nových konfigurací formátu souboru, které jsou odvozeny ze stávajícího modelu faktury

V tomto postupu vytvoříte konfigurace formátu souboru, které jsou nutné pro novou funkci elektronické fakturace, kterou chcete vytvořit. Můžete vytvořit konfiguraci formátu souboru elektronické faktury a jakékoli další konfigurace formátu souboru, které by vaše nová funkce elektronické fakturace mohla vyžadovat.

Než začnete tento postup, přihlaste se ke svému účtu Regulatory Configuration Service (RCS).

1. V Microsoft Dynamics 365 Finance v pracovním prostoru **Elektronické výkaznictví** vyberte **Úložiště** pro poskytovatele konfigurace **Microsoft**.
2. Vyberte **Globální**, vyberte **Otevřít** a poté v levém podokně vyberte konfiguraci **Model faktury**.

    > [!IMPORTANT]
    > Pro Brazílii vyberte místo toho konfiguraci modelu **Fiskální dokumenty**.

3. Na kartě **Konfigurace** vyberte **Import**.
4. Zavřete stránku.
5. Zavřete stránku.
6. Vyberte dlaždici **Konfigurace výkaznictví** a poté vyberte model faktury, který jste importovali.
7. Vyberte **Vytvořit konfiguraci** a poté vyberte **Formát založený na modelu kontextu faktury**.
8. Zadejte název a popis konfigurace formátu.
9. V poli **Typ formátu** vyberte typ přípony souboru.
10. Vyberte **Vytvořit konfiguraci** a pak vyberte konfiguraci formáu, kterou jste vytvořili.
11. Vyberte možnost **Návrhář** a pomocí nástroje návrháře formátu nakonfigurujte rozložení souboru tak, aby splňovalo specifikace formátu souboru.
12. Zavřete stránku.
13. Na kartě **Verze** vyberte možnost **Stav změny** \> **Dokončit**.
14. Vyberte **Změnit stav** \> **Sdílet** a publikujte konfiguraci formátu do globálního úložiště.

Nová konfigurace formátu souboru musí být sdílena s doménou Microsoft, než může být konfigurace používána službou elektronická fakturace.

1. Vyberte konfiguraci formátu, na které pracujete. Stav konfigurace musí být **Sdíleno**.
2. Na kartě **Verze** vyberte **Pokročilé sdílení** \> **Globální úložiště**.
3. Na kartě **Sdíleno s** vyberte **Organizace**.
4. V poli **Parametry** zadejte **Microsoft.com** a sdílejte konfiguraci formátu s doménou Microsoft.
5. Vyberte **OK**.

## <a name="create-the-new-electronic-invoicing-feature"></a>Vytvoření nové funkce elektronické fakturace

1. V RCS v pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **Elektronická fakturace**.
2. Vyberte **Přidat** a potom vyberte **Nová funkce**.
3. Zadejte název a popis funkce elektronické fakturace.
4. Vyberte **Vytvořit funkci**.

## <a name="add-electronic-invoicing-feature-configurations"></a>Přidání konfigurace funkce elektronické fakturace

1. Vyberte funkci elektronické fakturace, na které pracujete.
2. Na kartě **Konfigurace** vyberte **Přidat**.
3. V mřížce **Konfigurace** procházejte a vyberte konfigurace formátu souboru, které vaše funkce elektronické fakturace vyžaduje ke generování souboru elektronické faktury.
4. Vyberte **OK**.

## <a name="add-electronic-invoicing-feature-setups"></a>Přidání nastavení funkce elektronické fakturace

1. Na kartě **Nastavení** vyberte **Přidat** a poté vyberte **Vlastní nastavení**.
2. Zadejte název a popis nastavení funkce.
3. V poli **Typ nastavení** vyberte **Zpracování kanálu**.
4. Vyberte **Vytvořit**.
5. Vyberte nastavení, na kterém pracujete, a poté vyberte možnost **Upravit**.
6. Na kartě **Zpracování kanálu** vyberte **Nová** pro přidání akce kanálu. Další informace o kanálech naleznete v části [Akce](e-invoicing-configuration-rcs.md#actions).
7. Na kartě **Pravidla použitelnosti** vyberte **Nový** pro přidání klauzulí pravidel použitelnosti. Další informace o pravidlech použitelnosti naleznete v tématu [Pravidla použitelnosti](e-invoicing-configuration-rcs.md#applicability-rules).
8. Na kartě **Proměnné** vyberte **Nová** pro přidání proměnné podle potřeby.
9. Vyberte **Uložit** a poté vyberte **Ověřit** pro kontrolu konzistenci konfigurace.
10. Zavřete stránku.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>Nasazení funkce elektronické fakturace do prostředí služby

Informace o tom, jak tento úkol dokončit, najdete v tématu [Nasazení funkce elektronické fakturace do prostředí služby](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>Nasazení funkce elektronické fakturace do připojené aplikace

Informace o tom, jak tento úkol dokončit, najdete v tématu [Konfigurace nastavení aplikace](e-invoicing-get-started.md#configure-the-application-setup) a [Nasazení funkce elektronické fakturace do připojené aplikace](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).
