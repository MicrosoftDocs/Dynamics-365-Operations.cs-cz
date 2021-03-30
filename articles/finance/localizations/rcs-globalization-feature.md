---
title: Regulatory Configuration Services (RCS) - funkce globalizace
description: Toto téma vysvětluje, jak pomocí služby Microsoft Regulatory Configuration Services  (RCS) a globálního úložiště vytvářet a používat funkce globalizace.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: d5d42bd076ca77c5d2906593d44ae420d954a0b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218847"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Services (RCS) - funkce globalizace

[!include [banner](../includes/banner.md)]

Službu Microsoft Regulatory Configuration Services (RCS) můžete použít k vytvoření funkce globalizace, kterou lze použít v globalizačních službách, jako je například služba elektronické fakturace. RCS umožňuje provádět tyto úkoly:

- Definovat související komponenty funkce.
- Spravovat životní cyklus funkce prostřednictvím stavu funkce.
- Zpřístupnit funkci pro definované prostředí.
- Sdílet funkci s jinými organizacemi.

Následující postupy vysvětlují, jak může uživatel v RCS přidat funkci globalizace a související součásti, aktualizovat stav funkce a zpřístupnit tuto funkci tak, aby ji bylo možné použít ve službách globalizace.

Před dokončením postupů musíte provést kroky související s následujícími úkoly:

- Přístup k instanci RCS.
- Vytvoření a aktivace poskytovatele konfigurace. Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

V instanci aplikací Finance and Operations proveďte následující postup.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Nemáte-li pro vaši společnost zřízeno žádné RCS prostředí, pro její zřízení vyberte odkaz **Regulatory Services – Konfigurace** a postupujte podle pokynů.

> [!NOTE]
> Pokud již bylo pro vaši společnost zřízeno prostředí RCS, přejděte do prostředí pomocí adresy URL výběrem možnosti přihlášení.

## <a name="turn-on-the-globalization-features"></a>Zapnutí funkcí globalizace

1. V instanci RCS vyberte dlaždici **Správa funkcí**.
2. V pracovním prostoru **Správa funkcí** vyberte pracovní prostor **Funkce globalizace** v seznamu a poté vyberte **Povolit hned**.

    ![Funkce globalizace ve správě funkcí](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Globalizační funkce

Chcete-li použít funkci globalizace, musíte ji nejprve naimportovat z globálního úložiště a vytvořit si vlastní verzi. Existují dva způsoby, jak přidat funkce globalizace:

- Přidejte odvozenou funkci, která je založena na existující funkci, která byla publikována nebo sdílena.
- Přidejte novou funkci, kterou jste vytvořili od nuly.

## <a name="access-globalization-features"></a>Přístup k funkcím globalizace

1. Ujistěte se, že je funkce **Globalizační funkce** v okně Správa funkcí zapnutá, jak je popsáno dříve v tomto tématu.
2. Otevřete nový pracovní prostor **Globalizační funkce** a poté v části **Funkce** vyberte dlaždici **elektronická fakturace**.

    ![Pracovní prostor Globální funkce](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    Stránka **Funkce elektronické fakturace** je otevřená.

    ![Stránka Funkce elektronické fakturace](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Přidejte odvozenou funkci globalizace

Můžete přidat novou funkci globalizace odvozením z existující funkce, která byla publikována nebo sdílena.

1. Výběrem možnosti **Import** otevřete stránku **Import funkce z globálního úložiště**.

    ![Import funkce ze stránky Globální úložiště](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Výběrem volby **Synchronizovat** získáte nejnovější funkce.

    Synchronizovaný seznam obsahuje funkce, které máte k dispozici buď proto, že byly publikovány společností Microsoft, nebo proto, že byly s vámi sdíleny jiným poskytovatelem konfigurace.

    ![Synchronizovaný seznam funkcí](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. V seznamu vyberte funkce, které chcete importovat, a poté vyberte **Import**. Po úspěšném importu vybraných funkcí se zobrazí zpráva.

    ![Zpráva o úspěšném importu](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Vyberte **Přidat** a poté v rozevíracím seznamu vyberte možnost **Na základě stávající verze**.
5. Zadejte název a popis funkce.
6. V seznamu dostupných funkcí vyberte základní verzi funkce a poté vyberte **Vytvořit funkci**.

    ![Přidání odvozené funkce](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Funkce, kterou jste přidali, je vytvořena a má stav **Koncept**.

    ![Odvozená funkce, která má stav Koncept](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Zkontrolujte součásti funkcí a zjistěte, zda jsou vyžadovány aktualizace:

    - Prohlédněte si konfigurace v případě, že potřebujete přizpůsobit formáty elektronických zpráv (ER) a jejich vazby na mapování formátu pro verzi funkce.
    - Zkontrolujte nastavení, v případě, že potřebujete přizpůsobit kartu **Akce**, kartu **Pravidla použitelnosti** nebo kartu **Proměnné** pro pro verzi funkce.

8. Na kartě **Verze** vyberte datum **Účinné od** a zadejte popis, pokud je pole **Popis** prázdné.
9. Vyberte **Změnit stav** k dokončení funkce. Dokončené funkce mohou být zpřístupněny pro konkrétní prostředí, takže mohou být použity ve službách globalizace nebo mohou být publikovány do globálního úložiště.

> [!NOTE]
> Funkce, které mají hodnotu **Stav verze funkce** **Publikováno**, lze sdílet s externími organizacemi.

## <a name="add-a-new-globalization-feature"></a>Přidejte novou funkci globalizace

Můžete přidat novou funkci globalizace vytvořením od nuly.

1. Na stránce **Importovat funkci z globálního úložiště** vyberte **Přidat** a pak v dialogovém okně rozevíracího seznamu vyberte možnost **Nová funkce**.
2. Zadejte název a popis funkce.
3. Vyberte **Vytvořit funkci**.

    ![Přidání nové funkce](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. Na kartě **Verze** vyberte datum **Platné od** a pak výběrem možnosti **Změnit stav** funkci dokončete. Dokončené funkce mohou být zpřístupněny pro konkrétní prostředí, takže mohou být použity ve službách globalizace nebo mohou být publikovány do globálního úložiště.

> [!NOTE]
> Funkce, které mají hodnotu **Stav verze funkce** **Publikováno**, lze sdílet s externími organizacemi.

## <a name="feature-component-overview"></a>Přehled součástí funkce

Funkce globalizace mají několik součástí:

- **Verze** - Tato součást podporuje správu životního cyklu funkce a umožňuje uživatelům spravovat stav různých verzí této funkce.
- **Konfigurace** - Tato součást umožňuje uživatelům spravovat, prohlížet a upravovat související formáty ER a mapování formátů.
- **Nastavení** - Tato součást umožňuje uživatelům globalizačních služeb, jako je například elektronická fakturace, spravovat nastavení související verze funkce. Proto podporuje flexibilní sestavování pravidel komunikace a odpovědí.
- **Prostředí** - Tato součást umožňuje uživatelům globalizačních služeb, jako je například elektronická fakturace, spravovat prostředí, ve kterém se používá nastavení verze funkce, a udělit oprávnění uživatelům, kteří k nim budou mít přístup.
- **Organizace** - Tato součást umožňuje uživatelům sdílet tuto funkci s externími organizacemi.

## <a name="configuring-feature-components"></a>Konfigurace součástí funkcí

### <a name="version-and-status"></a>Verze a stav

Tato verze se používá ke správě životního cyklu funkce globalizace.

Stav lze změnit v poli **Stav** na kartě **Verze**. K dispozici jsou následující stavy:

- **Koncept** - Funkci lze upravit, pouze pokud je v tomto stavu.
- **Dokončit** - Funkce a všechny související součásti byly dokončeny (finalizovány) a nelze je upravovat.
- **Publikováno** - Funkce a všechny související součásti byly publikovány v globálním úložišti.
- **Sdíleno** - Funkce a všechny související součásti byly sdíleny s externími organizacemi.
- **Povoleno** - Funkce a všechny související součásti byly povoleny pro použití ve službě Globalizace, jako je služba elektronické fakturace.

> [!NOTE]
> Funkce se musí přes některé z těchto stavů postupně pohybovat. Proto nemusí být v každé fázi životního cyklu k dispozici každý stav.

### <a name="configurations"></a>Konfigurace

K dispozici jsou následující akce pro konfigurace:

- **Zobrazení** - Prohlédněte si základní konfigurace funkcí, které nevyžadují žádnou aktualizaci.
- **Upravit** - Vytvořte pracovní verzi vybrané konfigurace, abyste mohli upravovat formát nebo mapování formátu v Návrháři formátů.
- **Odstranit** - Odstranění vybrané konfigurace z funkce.
- **Přeskládat** - Přeskládejte funkci. Další informace naleznete v části [Přeskládání odvozených funkcí globalizace](#rebase) dále v tomto tématu.

### <a name="setups"></a>Nastavení

Pro nastavení funkcí jsou k dispozici následující akce:

- **Přidat** - Vytvoření nového nastavení funkce. Toto nastavení funkce lze odvodit z existujícího nastavení funkce nebo vytvořit od nuly.
- **Odstranit** - Odstraní vybrané nastavení funkce.
- **Zobrazit** - Zobrazí základní nastavení funkce, které nevyžaduje žádné změny.
- **Upravit** - Vytvoření, odstranění nebo úprava atributů tří hlavních součástí nastavení funkcí:

    - Akce a jejich parametry
    - Pravidla použitelnosti
    - Proměnné

![Stránka nastavení verze funkce](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Prostředí

K dispozici jsou následující akce pro prostředí:

- **Povolit** - U vybrané verze funkce vyberte publikované prostředí a vyberte datum **Platnost od**, odkdy by mělo být k dispozici. Další informace naleznete v části [Konfigurace prostředí pro povolení](#configureenvironment) dále v tomto tématu.
- **Zrušit** - Odebere prostředí pro nastavení funkce.

### <a name="organizations"></a>Organizace

Chcete-li sdílet funkci globalizace s externí organizací, postupujte takto.

1. Na stránce **Funkce elektronické fakturace** vyberte funkci a verzi funkce, kterou chcete sdílet.
2. Na kartě **Organizace** vyberte **Sdílet s** a poté v rozevíracím seznamu zadejte název domény organizace.
3. Vyberte **Sdílet**.

    ![Sdílení funkce s organizací.](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Funkce je sdílena s vybranou organizací a je k dispozici této organizaci v globálním úložišti. Odtud lze funkci importovat do instance RCS organizace nebo Dynamics 365 Finance, aby mohla být použita.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Přeskládání odvozené funkce globalizace

Odvozenou funkci globalizace můžete znovu převést na novou nebo aktualizovanou základní verzi funkce. Tímto způsobem lze automaticky aktualizovat změny, ke kterým došlo v základní verzi. Aktualizovaná verze základní funkce je vytvořena původním poskytovatelem konfigurace a poté je publikována nebo sdílena.

![Aktualizovaná verze základní funkce](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Pokud například chcete znovu převést odvozenou verzi funkce, kterou jste vytvořili, nejprve získáte nejnovější verzi funkce importem z globálního úložiště.

1. Na stránce **Funkce elektronické fakturace** vyberte **Import**.
2. Výběrem volby **Synchronizovat** získáte nejnovější funkce.
3. V seznamu funkcí vyberte funkce, které chcete importovat, a poté vyberte **Import**.

    ![Import nejnovější verze funkce](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. V seznamu funkcí vyberte funkci, kterou chcete obnovit.
5. Na kartě **Verze** vyberte **Nový** pro vytvoření rámcové verze.

    ![Vytvořená nová rámcová verze](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Vyberte **Přeskládat**.
7. V dialogovém okně **Přeskládat** vyberte nejnovější verzi funkce, na kterou chcete znovu přejít.

    ![Dialogové okno Přeskládat](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Vyberte **OK**.
9. Zkontrolujte součásti funkce a proveďte požadované změny.
10. Vyberte **Změnit stav** k dokončení funkce přeskládání. Po dokončení přeskládání můžete provádět další akce. Tuto funkci můžete například zveřejnit a zpřístupnit ji pro použití v globalizačních službách.

    ![Stav funkce byl aktualizován na Dokončeno](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Konfigurace prostředí pro funkce globalizace

Uživatelé globalizačních služeb mohou spravovat prostředí, aby nastavili funkci globalizace a udělili oprávnění ostatním uživatelům, kteří k ní budou mít přístup.

1. V pracovním prostoru **Funkce globalizace** v části **prostředí** vyberte dlaždici **elektronická fakturace**.

    ![Pracovní prostor Funkce globalizace](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Vyberte **Parametry úložiště klíčů** a poté výběrem možnost **Nový** vytvořte tajné úložiště klíčů Azure.
3. Zadejte název a popis úložiště klíčů a poté do pole **URI úložiště klíčů** zadejte adresu URL, která identifikuje prostředek úložiště klíčů v Azure.
4. Na pevné záložce **Certifikáty** vyberte **Přidat** pro přidání certifikátu a zadejte název a popis každého certifikátu.

    ![Certifikát byl přidán](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Vyberte **Nový** pro vytvoření nového prostředí.
6. Zadejte název, popis a tajný token podpisu sdíleného přístupu požadovaný pro úložiště.
7. Na pevné záložce **Uživatelé** vyberte **Nový** pro přidání uživatele, který bude mít oprávnění pro přístup do tohoto prostředí.
8. Zadejte ID a e-mailovou adresu uživatele.
9. Chcete-li přidat další uživatele, zopakujte kroky 7 a 8.
10. Výběrem možnosti **Publikovat** publikujte prostředí.

    ![Publikované prostředí](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]