---
title: Vytvoření funkce globalizace
description: Toto téma vysvětluje, jak vytvořit funkci globalizace.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 197a5b983b307758425b1acc1f354d0a8bfbf8a1
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371580"
---
# <a name="create-a-globalization-feature"></a>Vytvoření funkce globalizace

[!include [banner](../includes/banner.md)]

Funkci elektronické fakturace můžete vytvořit buď úplně od začátku, nebo ji založit na jiné stávající funkci. Když vytvoříte funkci od začátku, musíte ručně přidat konfigurace a jiné komponenty Elektronické fakturace (ER), například nastavení funkce a detaily nastavení aplikace. Když vytvoříte funkci, která je založena na stávající funkci, nový prvek zdědí všechny konfigurace a parametry základní funkce. Můžete přitom zkontrolovat, co se zkopíruje ze základní funkce do nové.

## <a name="create-a-feature-from-scratch"></a>Vytvoření funkce od začátku

Tato sekce vysvětluje, jak vytvořit funkci elektronické fakturace, když pro vaše obchodní scénáře není k dispozici žádná integrovaná funkce globalizace v globálním úložišti.

Chcete-li vytvořit funkci elektronické fakturace, postupujte takto.

1. Přihlaste se ke svému účtu Regulatory Configuration Service (RCS).
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **Elektronická fakturace**.
3. Vyberte **Přidat** a poté v rozevíracím seznamu vyberte možnost **Nová funkce**.
4. Zadejte název a popis funkce elektronické fakturace.
5. Vyberte **Vytvořit funkci**. První verze nové funkce se zobrazí na pravé straně stránky a má stav **Koncept**.

    Dále musíte přidat konfigurace ER a nastavení funkcí. Než přidáte nové nebo stávající konfigurace formátu ER, ujistěte se, že existují ve vašem místním úložišti RCS.

6. Vyberte funkci elektronické fakturace, na které pracujete.
7. Na kartě **Konfigurace** vyberte **Přidat**.
8. V mřížce **Konfigurace** vyhledejte a vyberte konfigurace formátu, které jsou vyžadovány pro kanál zpracování (například pro generování souborů elektronických faktur nebo zpracování odpovědí z externích webových služeb).
9. Vyberte **OK**. Nyní můžete použít konfigurace v akcích kanálu zpracování. Další informace získáte v části [Práce s konfiguracemi](e-invoicing-work-configurations.md).
10. Chcete-li přidat nastavení funkce elektronické fakturace, vytvořte ho na kartě **Nastavení** stránky **Nová funkce**. Další informace naleznete v tématu [Práce s nastavením funkcí](e-invoicing-feature-setup.md).
11. Dokončete nastavení a nasaďte funkci elektronické fakturace do prostředí služby. Další informace najdete v tématu [Dokončení, publikování a nasazení funkce globalizace](e-invoicing-complete-publish-deploy-globalization-feature).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Vytvoření konfigurací formátu souboru, které jsou odvozeny ze stávajícího modelu faktury

Tuto část můžete přeskočit, pokud nemusíte vytvářet konfigurace ER, ale můžete znovu použít existující verze jako základ.

Tato procedura ukazuje, jak vytvořit konfigurace formátu souboru, které jsou nutné pro novou funkci elektronické fakturace, kterou chcete vytvořit. Vytvořte konfiguraci formátu souboru elektronické faktury a jakékoli další konfigurace formátu souboru, které vaše nová funkce elektronické fakturace vyžaduje.

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
3. Vyberte položku **Model faktury** nebo u scénářů pro Brazílii položku **Fiskální model**.
4. Vyberte možnost **Vytvořit konfiguraci** a poté v rozevíracím dialogovém okně vyberte možnost **Formát založený na datovém modelu Faktura**.
5. Zadejte název a popis konfigurace formátu.
6. V poli **Typ formátu** vyberte typ přípony souboru.
7. V poli **Definice datového modelu** vyberte kořenovou strukturu, na kterou chcete formát namapovat. Například **InvoiceCustomer** se používá pro formáty faktur zákazníka.
8. Vyberte **Vytvořit konfiguraci**.
9. Zvolte novou konfiguraci formátu.
10. Vyberte možnost **Návrhář** a pomocí nástroje návrháře formátu nakonfigurujte rozložení souboru tak, aby splňovalo specifikace formátu souboru.
11. Zavřete stránku.
12. Na kartě **Verze** vyberte možnost **Stav změny** \> **Dokončit**.
13. Vyberte **Změnit stav** \> **Sdílet** a publikujte konfiguraci formátu do globálního úložiště.

Nové konfigurace formátu souboru musejí být sdíleny s doménou Microsoft, než mohou být používány službou elektronická fakturace.

1. Vyberte konfiguraci formátu, na které pracujete. Stav konfigurace musí být **Sdíleno**.
2. Na kartě **Verze** vyberte **Pokročilé sdílení** \> **Globální úložiště**.
3. Na kartě **Sdíleno s** vyberte **Organizace**.
4. V poli **Parametry** zadejte **microsoft.com** a sdílejte konfiguraci formátu s doménou Microsoft.
5. Vyberte **OK**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Vytvoření funkce, která je založena na stávající funkci

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **Elektronická fakturace**.
3. V poli **Poskytovatel konfigurace** zkontrolujte, že je vybrán aktivní poskytovatel konfigurace. Tímto způsobem se nová funkce elektronické fakturace objeví v seznamu po jejím vytvoření. Pokud váš aktivní poskytovatel konfigurace není vybrán, bude nová funkce ze seznamu odfiltrována.
4. Vyberte **Přidat** a poté v rozevíracím seznamu vyberte možnost **Na základě stávající verze**.
5. Zadejte název a popis funkce.
6. V poli **Základní funkce** vyberte základní verzi funkce.
7. Vyberte **Vytvořit funkci**. Funkce je vytvořena a má stav **Koncept**.
8. Zkontrolujte součásti funkcí a zjistěte, zda jsou vyžadovány aktualizace:

    - Zkontrolujte konfigurace v případě, že musíte přizpůsobit formáty ER a jejich vazby na mapování formátu pro verzi funkce.
    - Zkontrolujte nastavení, v případě, že musíte pro verzi funkce přizpůsobit kartu **Akce**, kartu **Pravidla použitelnosti** nebo kartu **Proměnné**.

9. Dokončete nastavení a nasaďte funkci elektronické fakturace do prostředí služby. Další informace najdete v tématu [Dokončení, publikování a nasazení funkce globalizace](e-invoicing-complete-publish-deploy-globalization-feature).
