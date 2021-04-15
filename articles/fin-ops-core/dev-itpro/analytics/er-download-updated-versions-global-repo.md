---
title: Import aktualizovaných verzí konfigurací ER
description: Toto téma vysvětluje, jak importovat aktualizované verze konfigurací elektronického vykazování (ER) z globálního úložiště konfigurační služby.
author: NickSelin
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 1e021105c19273db5ded7cb0902eca1d502ced8e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753353"
---
# <a name="import-updated-versions-of-er-configurations"></a>Import aktualizovaných verzí konfigurací ER

[!include [banner](../includes/banner.md)]

[Úložiště](general-electronic-reporting.md#Repository) elektronického výkaznictví (ER) se používají ke sdílení [konfigurací ER](general-electronic-reporting.md#Configuration). Můžete [importovat](download-electronic-reporting-configuration-lcs.md) konfigurace ER z různých úložišť do vaší instance Microsoft Dynamics 365 Finance. Při importu konfigurací ER mohou [poskytovatelé konfigurací](general-electronic-reporting.md#Provider) publikovat nové [verze](general-electronic-reporting.md#component-versioning) v úložištích, aby bylo možné je sdílet.

Toto téma vysvětluje, jak importovat aktualizované verze konfigurací ER z globálního úložiště konfigurační služby. Další informace viz [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, konfigurační služba](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Kontrola dostupných aktualizovaných verzí

1. Přihlaste se k aplikaci Finance použitím některé z následující role:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Import aktualizovaných verzí konfigurací**.

    ![Stránka konfigurací lokalizace](./media/er-download-updated-versions-global-repo1.png)

4. V dialogovém okně **Import aktualizovaných verzí konfigurací elektronického výkaznictví** vyberte v poli **Režim spouštění** možnost **Zobrazit pouze dostupné aktualizace**. Pak vyberte **OK**. 

    ![Pole Režim spuštění s hodnotou Zobrazit pouze dostupné aktualizace](./media/er-download-updated-versions-global-repo2.png)

5. Zkontrolujte zprávy, které obdržíte. Tyto zprávy uvádějí následující informace o konfiguracích ER v aktuální instanci systému Finance a o tom, jak srovnávají s obsahem globálního úložiště:

    - Celkový počet konfigurací ER
    - Konfigurace ER, které nejsou přítomny v globálním úložišti
    - Konfigurace ER, pro které je aktuální verze již k dispozici v aktuální instanci systému Finance (chcete-li zobrazit úplný seznam těchto konfigurací ER, klikněte na odkaz **Podrobnosti zprávy**)

        ![Zpráva „Nejnovější verze následujících konfigurací již byly importovány“ a podrobnosti zprávy](./media/er-download-updated-versions-global-repo3.png)

    - Konfigurace ER, pro které je aktuální verze již k dispozici v globálním úložišti a jež lze importovat do aktuální instance systému Finance (chcete-li zobrazit úplný seznam těchto konfigurací ER, klikněte na odkaz **Podrobnosti zprávy**)

        ![Zpráva „Dostupné aktualizace“ a podrobnosti zprávy](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Import dostupných aktualizovaných verzí

1. Přihlaste se k aplikaci Finance použitím některé z následující role:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Import aktualizovaných verzí konfigurací**.
4. V dialogovém okně **Import aktualizovaných verzí konfigurací elektronického výkaznictví** vyberte v poli **Režim spouštění** možnost **Importovat nejnovější aktualizace**. Provede se import nejnovějších verzí konfigurací ER z globálního úložiště do aktuální instance systému Finance.
5. Chcete-li naplánovat dávkovou úlohu importu, nastavte na záložce s náhledem **Spustit na pozadí** u možnosti **Dávkové zpracování** hodnotu **Ano**. Pokud chcete import opakovat pravidelně, nakonfigurujte požadované opakování.

    ![Pole Režim spouštění nastavené na Import nejnovějších aktualizací](./media/er-download-updated-versions-global-repo5.png)

6. Vyberte **OK**.
7. Chcete-li zjistit, jaké verze konfigurací byly importovány, postupujte takto:

    - Pokud import spustíte interaktivně místo použití dávkové úlohy, zkontrolujte zprávy, které obdržíte.

        ![Zprávy přijaté během interaktivního importování](./media/er-download-updated-versions-global-repo6.png)

    - Pokud spouštíte import v dávkovém režimu, postupujte takto:

        1. Přejděte na **Společné** \> **Dotazy** \> **Dávkové úlohy** \> **Moje dávkové úlohy**.
        2. Vyhledejte a vyberte úlohu **Import aktualizací verzí konfigurací elektronického výkaznictví** a poté v podokně Akce vyberte na kartě **Dávková úloha** možnost **Historie dávkových úloh**. Zobrazí se historie úloh.
        3. Na stránce **Historie dávkových úloh** vyberte možnost **Protokol**. Poté v obdržené zprávě klikněte na odkaz **Podrobnosti zprávy**. Zobrazí se protokol úlohy.

        ![Protokol úlohy](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Nedoporučujeme plánovat opakovanou dávkovou úlohu tak, aby importovala aktualizované verze konfigurací ER přímo z globálního úložiště do produkčního prostředí, protože importované verze budou okamžitě k dispozici k použití. Místo toho tímto postupem přeneste verze konfigurací ER do prostředí sandbox. Poté je můžete vyhodnotit v prostředí sandbox a teprve následně nasadit do produkčního prostředí.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]