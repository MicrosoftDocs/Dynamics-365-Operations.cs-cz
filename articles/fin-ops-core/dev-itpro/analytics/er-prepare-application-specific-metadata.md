---
title: Příprava metadat specifických pro aplikaci pro RCS a ER
description: V tomto tématu je vysvětleno, jak připravit metadata specifická pro aplikaci pro službu Regulatory Configuration Service (RCS) a elektronické výkaznictví (ER).
author: NickSelin
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f0501fd67da0cbc5c10171b55004cb7f4fd4fd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743696"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a>Příprava metadat specifických pro aplikaci pro RCS a ER

[!include[banner](../includes/banner.md)]

V tomto tématu jsou uvedeny příklady následujících úloh:

- [Příprava metadat aplikace k použití v RCS](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Přístup k metadatům aplikace pomocí konfigurace elektronického výkaznictví](#access-application-metadata-by-using-an-er-configuration)
- [Přístup k metadatům aplikace pomocí připojených aplikací](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>Příprava metadat aplikace k použití v RCS

V následujícím postupu je ukázáno, jak může uživatel, který má oprávnění **Správce systému** nebo **Vývojář elektronického výkaznictví** vytvořit konfiguraci elektronického výkaznictví (ER) obsahující metadata pro aplikaci , která se používá k návrhu konfigurací mapování modelu ER v rámci služby Regulatory Configuration Service (RCS). Ukázková konfigurace mapování modelu ER vytvořená v tomto příkladu bude použita pro přístup k transakcím zahraničního obchodu.

V tomto příkladu chcete použít RCS pro návrh řešení ER pro aplikaci, které bude použito k vygenerování elektronických dokumentů, které obsahují informace z cizí obchodní domény. Chcete-li určit mapování mezi datovým modelem ER a zdroji požadovaných dat, musíte mít přístup k metadatům aplikace v RCS. Proto je v rámci procesu navrhování řešení ER nutné nakonfigurovat novou konfiguraci metadat ER, která obsahuje všechna metadata aktuálně požadovaná k vygenerování sestav ER pro vybranou obchodní doménu.

> [!NOTE]
> V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v libovolné společnosti.

1. Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.
2. Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření zprostředkovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Vyberte **Konfigurace metadat**.
4. Vyberte **Vytvořit konfiguraci**.
5. V rozevíracím dialogovém okně do pole **Název** zadejte název. V tomto příkladu zadejte **metadata zahraničního obchodu**.
6. Vyberte **Vytvořit konfiguraci**.
7. Vyberte možnost **Návrhář**.
8. Vyberte **přidat**.

    > [!NOTE]
    > Můžete vybrat všechna metadata buď pro celou aplikaci, nebo pro vybrané modely nebo moduly. V obou případech je třeba mít na paměti, že následující metadata budou automaticky přidána: tabulky záznamů, výčty a rozšířené datové typy (EDT). Pokud jsou požadovány další typy metadat, musí být přidány ručně.

    Je nutné přidat metadata, která se vztahují k transakcím zahraničního obchodu, a ručně vybrat položky metadat.

9. Vyberte **Přidat zdroj dat \> Záznamy tabulky**.
10. Vyfiltrujte hodnotu **Intrastat** v poli **Název**.
11. Vyberte záznam tabulky **Intrastat**.
12. Vyberte **OK**.

    Je nutné přidat informace o metadatech do tabulky záznamů Intrastat.

13. Ve stromové struktuře vyberte **Intrastat záznamů tabulky \> \>Vztahy \> IntrastatCommodity (záznamy tabulky EcoResCategory)**.
14. Vyberte **Přidat metadata**.

    > [!NOTE]
    > Metadata o požadovaných vztazích pro vybranou tabulku záznamů je nutné přidat ručně.

15. Vyberte **Přidat zdroj dat**.
16. Vyberte **Výčet**.
17. Vyfiltrujte hodnotu **IntrastatDirection** v poli **Název**.
18. Vyberte záznam výčtu **IntrastatDirection**.
19. Vyberte **OK**.
20. Zvolte **Uložit**.
21. Zavřete stránku.
22. Dokončete návrh konceptu konfigurace metadat:

    1. Vyberte **Změnit stav \> Dokončeno**.
    2. Vyberte **OK**.
    3. Vyberte dokončenou verzi 1.

23. Exportujte dokončenou verzi konfigurace metadat z aplikace do souboru XML:

    1. Vyberte **Exchange \> Exportovat jako soubor XML**.
    2. Vyberte **OK**.

Konfigurace metadat ER, kterou jste vytvořili, je uložena jako **Metadata zahraničního obchodu.xml**. Nyní jej můžete importovat do RCS, aby jej bylo možné použít jako zdroj metadat pro obchodní doménu zahraničního obchodu. Na základě těchto informací můžete určit mapování mezi metadaty aplikací a datovým modelem ER.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Přístup k metadatům aplikace pomocí konfigurace elektronického výkaznictví

Následující postup ukazuje, jak může uživatel RCS, který má roli **Správce systému** nebo **Vývojář elektronického výkaznictví**, navrhnout nové mapování modelu ER pomocí metadat z aplikace. K metadatům aplikace se přistupuje pomocí konfigurace metadat ER, která obsahuje ukázkovou sadu metadat pro přístup k transakcím zahraničního obchodu.

Než budete moci tuto proceduru dokončit, je nutné dokončit nejprve následující procedury:

- [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [Příprava metadat aplikace k použití v RCS](#prepare-application-metadata-that-can-be-used-in-rcs)

1. Přejděte na **Všechny pracovní prostory \> Elektronické výkaznictví**.
2. Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření zprostředkovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Importujte konfiguraci metadat ER obsahující metadata z aplikace, která je nakonfigurována pro generování elektronických dokumentů pro doménu zahraničního obchodu. Tato konfigurace metadat ER byla vytvořena a exportována jako soubor XML v proceduře [Příprava metadat aplikace, která lze použít v proceduře RCS](#prepare-application-metadata-that-can-be-used-in-rcs) dříve v tomto tématu.

    1. Vyberte **Konfigurace metadat**.
    2. Vyberte **Exchange**.
    3. Vyberte **Načíst ze souboru XML**.
    4. Klikněte na Procházet a vyberte soubor **Foreign trade metadata.xml**.
    5. Vyberte **OK**.
    6. Zavřete stránku.

4. Vytvoření konfigurace datového modelu:

    1. Vyberte **Konfigurace vykazování**.
    2. Vyberte **Vytvořit konfiguraci**.
    3. V rozevíracím dialogovém okně do pole **Název** zadejte **Model zahraničního obchodu**.
    4. Vyberte **Vytvořit konfiguraci**.
    5. Vyberte možnost **Návrhář**.
    6. Kliknutím na možnost **Nový** otevřete dialogové okno.

        1. Do pole **Název** zadejte **Kořen**.
        2. Vyberte **přidat**.
    
    7. Kliknutím na možnost **Nový** otevřete dialogové okno.

        1. Do pole **Název** zadejte **Transakce**.
        2. V poli **Typ položky** vyberte **Seznam záznamů**.
        3. Vyberte **přidat**.
 
    8. Kliknutím na možnost **Nový** otevřete dialogové okno.

        1. Do pole **Název** zadejte **Kód komodity**.
        2. V poli **Typ položky** vyberte **Řetězec**.
        3. Vyberte **přidat**.

    9. Kliknutím na možnost **Nový** otevřete dialogové okno.

        1. Do pole Název zadejte **Fakturovaná částka**.
        2. V poli **Typ položky** vyberte **Reálný**.
        3. Vyberte **přidat**.

    10. Kliknutím na možnost **Nový** otevřete dialogové okno.

        1. Do pole **Název** zadejte **Datum**.
        2. V poli **Typ položky** vyberte **Datum**.
        3. Vyberte **přidat**.
 
    11. Vyberte **Přidat \> Kořenová reference**.
    12. Vyberte **OK**.
    13. Zvolte **Uložit**.
    14. Zavřete stránku.
    15. Vyberte **Změnit stav \> Dokončeno**.
    16. Vyberte **OK**.

5. Vytvoření konfigurace mapování modelu:

    1. Vyberte **Vytvořit konfiguraci**.
    2. V rozevíracím dialogovém okně zadejte do pole **Nový** **Mapování modelu založené na datovém modelu Model zahraničního obchodu**.
    3. Do pole **Název** zadejte **Mapování zahraničního obchodu**'.
    4. Vyberte **Vytvořit konfiguraci**.
    5. Na pevné záložce **Předpoklady** vyberte **Upravit**.
    6. Zvolte **Nové**.
    7. V poli **Typ komponenty předpokladu** vyberte **Konfigurace**.
    8. Vyberte konfiguraci **Metadat zahraničního obchodu**.
    9. Zvolte **Uložit**. Všimněte si, že jsme přidali odkaz na verzi 1 konfigurace **Metadata zahraničního obchodu**. Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo.
    10. Zavřete stránku.
    11. Vyberte možnost **Návrhář**.
    12. Vyberte možnost **Návrhář**.
    13. Ve stromovém zobrazení vyberte **Dynamics 365 for Operations \> Záznamy tabulky**.
    14. Vyberte **Přidat kořen**.
    15. Do pole **Název** zadejte **Intrastat**.
    16. Vyberte záznamy tabulky **Intrastat**.
    17. Vyberte **OK**.

        > [!NOTE]
        > Jsou nabídnuty pouze dvě tabulky, protože do sady metadat, která je právě používána, byly přidány pouze dvě tabulky.

    18. Vyberte možnost **vazba**.
    19. Ve stromovém zobrazení vyberte **Intrastat \> AmountMST**.
    20. Ve stromovém zobrazení vyberte možnost **Transakce = Intrastat \> Fakturovaná částka**.
    21. Vyberte možnost **vazba**.
    22. Ve stromovém zobrazení vyberte **Intrastat \> TransDate**.
    23. Ve stromovém zobrazení vyberte **Transakce = Intrastat \> Date**.
    24. Vyberte možnost **vazba**.
    25. Ve stromovém zobrazení vyberte **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.
    26. Ve stromovém zobrazení vyberte **Transakce = Intrastat \> Commodity code**.
    27. Vyberte možnost **vazba**.
    28. Vyberte **Ověřit**.

        > [!NOTE]
        > Po ověření jste úspěšně jsme provedli vázání prvků datového modelu s položkami datových zdrojů, které jsou popsány pomocí podrobností metadat aplikace z odkazované konfigurace metadat ER.

    29. Zvolte **Uložit**.

Podle požadavku můžete rozšířit existující sadu metadat v aplikaci Poté můžete exportovat novou dokončenou verzi konfigurace metadat ER, importovat ho do RCS a aktualizovat předpoklady konfigurace konfigurovaného mapování modelu odkazující na novou verzi importované konfigurace metadat.

> [!NOTE]
> Tento způsob získání informací o metadatech aplikace je jediný dostupný pro lokálně nasazené aplikace (v případě místních obchodních dat \[LBD\] nebo místně, model nasazení se používá pro aplikaci).

## <a name="access-application-metadata-by-using-connected-applications"></a>Přístup k metadatům aplikace pomocí připojených aplikací

Následující postup ukazuje, jak může uživatel RCS, který má roli **Správce systému** nebo **Vývojář elektronického výkaznictví**, navrhnout nové mapování modelu ER pomocí metadat aplikace. Přístup k metadatům aplikace bude probíhat online pomocí aplikace připojené k RCS. Ukázkové mapování modelu ER bude konfigurováno pro přístup k transakcím zahraničního obchodu.

K provedení kroků v tomto postupu musíte nejprve dokončit proceduru [Vytvoření zprostředkovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md) v RCS. Pokud jste nedokončili kroky uvedené v tématu [Přístup k metadatům aplikace pomocí konfigurace ER](#access-application-metadata-by-using-an-er-configuration), přejděte na stránku [Příklady elektronického výkaznictví Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) a stáhněte a uložte následující konfigurace ER a uložte je místně: **Foreign trade metadata.xml**, **Foreign trade model.xml** a **Foreign trade mapping.xml**.


### <a name="get-required-er-configurations"></a>Získání požadovaných konfigurací ER

Pokud jste již provedli kroky v postupu [Přístup k metadatům aplikace pomocí konfigurace ER](#access-application-metadata-by-using-an-er-configuration) dříve v tomto tématu, již máte v aktuální instanci RSC všechny potřebné konfigurace ER (konfigurace metadat pro zahraniční obchod, model a mapování). V takovém případě můžete tento postup vynechat.

1. Přejděte na **Všechny pracovní prostory \> Elektronické výkaznictví**.
2. Vyberte **Konfigurace vykazování**.
3. Načtěte soubory konfigurace **Foreign trade metadata.xml**, **Foreign trade model.xml** a **Foreign trade mapping.xml** opakující následující řetězec kroků pro každý z nich:

    1. Vyberte **Exchange**.
    2. Vyberte **Načíst ze souboru XML**.
    3. Vyberte **Procházet** a vyberte soubor.
    4. Vyberte **OK**.

### <a name="register-the-connection-with-the-application"></a>Zaregistrovat připojení k aplikaci

1. Přejděte na **Všechny pracovní prostory \> Elektronické výkaznictví**.
2. Vyberte **Připojené aplikace**.
3. Ujistěte se, že konfigurovaná aplikace je založena na Microsoft Azure a že je obecně přístupná uživatelům RCS. Aktuální uživatel RCS musí mít přístup k vybrané aplikaci a být zaregistrován jako uživatel této aplikace, který má roli poskytující mu oprávnění pro přístup k metadatům aplikace.
4. Zvolte **Nové**.
5. Do pole **Název** zadejte **MyConnectedApp** jako název připojené aplikace.
6. V poli **aplikace** zadejte adresu URL aplikace.
7. V poli **Tenant** zadejte poskytovatele aplikace.
8. Zvolte **Uložit**. 
9. Při kontrole připojení ke konfigurované aplikaci vyberte stránce **Připojit ke vzdálené aplikaci na** odkaz **Kliknutím sem se připojte k vybrané aplikaci**. 
10. Chcete-li ověřit přístup ke konfigurované aplikaci, vyberte možnost **Zkontrolovat připojení**.
11. Vyberte **Zavřít**.

Po dokončení této procedury a ověření úspěšného připojení budou podrobnosti o verzi a klientovi pro konfigurovanou aplikaci v aktuální mřížce aktualizovány.

### <a name="review-the-existing-model-mapping-configuration"></a>Kontrola existující konfigurace mapování modelu ER

1. Přejděte na **Všechny pracovní prostory \> Elektronické výkaznictví**.
2. Vyberte **Konfigurace vykazování**.
3. Ve stromové struktuře vyberte **Model zahraničního obchodu \> Mapování zahraničního obchodu**.
4. Na pevné záložce **Předpoklady** vyberte Upravit.

    > [!NOTE]
    > V současné době toto mapování odkazuje na konfiguraci metadat. Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo.

4. Vyberte možnost **Návrhář**.
5. Vyberte možnost **Návrhář**.
6. Ve stromovém zobrazení vyberte **Dynamics 365 for Operations \> Záznamy tabulky**.
7. Vyberte **Přidat kořen**.
8. V poli **Tabulka** zadejte nebo vyberte hodnotu.

    > [!NOTE]
    > V současné době toto mapování odkazuje na konfiguraci metadat. Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo.

9. Vyberte možnost **Zrušit**.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>Přiřazení připojené aplikace k mapování modelu

1. Vyberte možnost **Upravit**.
2. V **poli Připojená aplikace** vyberte aplikaci **MyConnectedApp**.

    > [!NOTE]
    > Toto mapování odkazuje na metadata vybrané připojené aplikace. Pokud stejné mapování odkazuje na konfiguraci metadat a připojenou aplikaci současně, budou použita metadata připojené aplikace.

3. Vyberte možnost **Návrhář**.
4. Vyberte možnost **Návrhář**.
5. Ve stromovém zobrazení vyberte **Dynamics 365 for Operations \> Záznamy tabulky**.
6. Vyberte **Přidat kořen**.
7. V poli **Tabulka** zadejte nebo vyberte hodnotu.

    > [!NOTE]
    > Nyní byly nabídnuty více než dvě tabulky aplikace, protože toto mapování používá všechna metadata připojené aplikace, která je k ní přiřazena.

8. Vyberte možnost **Zrušit**.
9. Vyberte **Ověřit**.

Úspěšně jste provedli vázání prvků datového modelu s položkami datových zdrojů, které jsou popsány pomocí podrobností metadat připojené aplikace, která byla přiřazena pro toto mapování.

Potřebujete-li vyhodnotit mapování modelu pomocí metadat jiné verze aplikace, zaregistrujte jinou připojenou aplikaci, přiřaďte ji k tomuto mapování modelu a ověřte ji proti novým metadatům.

## <a name="additional-resources"></a>Další zdroje

Případně můžete přehrát Průvodce záznamem úloh **Připravit metadata aplikace, která lze použít v RCS** v aplikaci a **Přístup k metadatům aplikace pomocí konfigurace ER** a **Přístup k metadatům aplikace pomocí připojených aplikací** v RCS. Tyto Průvodce záznamem úloh je možné stáhnout ze stránky [Průvodci záznamem úloh pro Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]