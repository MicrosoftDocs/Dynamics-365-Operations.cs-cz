---
title: Nábor uchazečů o práci
description: Tento článek popisuje, jak nabírat kandidáty v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 743c78d3526db2707630229d4cf21531f9641dd6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879243"
---
# <a name="recruit-job-candidates"></a>Nábor uchazečů o práci


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources vám pomůže spravovat žádosti o nábor. Pomůže vám také s bezproblémovým přechodem uchazečů o zaměstnání na zaměstnance. Pokud vaše organizace používá samostatnou náborovou aplikaci, může váš náborový proces zahrnovat následující kroky:<!--note from editor: Should this be a numbered list? These steps do seem to follow a particular order.-->

- Zadejte svou žádost o nábor v Human Resources.
- Přijměte doporučení kandidátů v Human Resources z náborové aplikace.
- Dokončete proces schvalování kandidátů v Human Resources.

Pokud nepoužíváte samostatnou náborovou aplikaci, můžete kandidáty spravovat také ručně v Human Resources.

> [!NOTE]
> Pokud jste správcem nebo vývojářem a chcete integrovat Human Resources s náborovou aplikací jiných výrobců, jděte na [Konfigurace integrace Dataverse](hr-admin-integration-common-data-service.md) a [Konfigurace virtuálních tabulek Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Najdete zde také náborové integrační aplikace v [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
## <a name="enable-recruiting-requests-on-the-merged-infrastructure"></a>Povolení požadavků na nábor ve sloučené infrastruktuře

Pokud chcete podat žádosti o nábor v náboru lidských zdrojů, musíte nejprve povolit funkce **Uživatelské prostředí HR** a **Řízení procesu náboru**.

Jakmile jsou funkce zapnuté, vyberte je pomocí následujících kroků: 
1. Jděte na **Lidské zdroje** > **Nastavení** > **Parametry lidských zdrojů**.
2. Na kartě  **Nábor**  nastavte pole **Nábor povolen** na **Ano**.
3. V rozevíracím seznamu **Zkušenosti s náborem** vyberte **Nábor HR**.  
4. Klikněte na tlačítko **Uložit**. 

> [!Note] 
> Po výběru **Nábor HR** nebude pole **Projekty náboru** (zastaralé) k dispozici. 


## <a name="add-a-recruiting-request-location"></a>Přidání umístění žádosti o nábor

Pokud má vaše organizace více umístění, můžete je přidat, aby si žadatelé mohli vybrat místo, kde bude nový nábor probíhat. Umístění bude zahrnuto do publikovaného pracovního místa.

1. Do vyhledávacího pole zadejte **Umístění žádosti o nábor**.
2. Zvolte **Nové**.
3. V poli **Umístění žádosti o nábor** zadejte název umístění.

    ![Přidání umístění žádosti o nábor.](./media/hr-recruit-0a-add-location.png)

4. Do pole **Popis** zadejte popis umístění.
5. Ve volbě **Umístění** vyberte **Přidat**. Pokud se objeví dialogové okno **Nová adresa**, zadejte adresu umístění.<!--note from editor: Please make the address in this image less plausible. Via the fictitious guidelines on CELAweb: For street addresses, you should use sequential numbers, common street names, and incorrect zip codes (e.g., 4567 Main St Buffalo, NY 98052). (See https://microsoft.sharepoint.com/sites/CELAWeb-Copyrights-Trademarks-And-Patents/SitePages/trademarks-fictitious-names.aspx)-->

    ![Zadejte adresu.](./media/hr-recruit-0b-address.png)

6. Pod **Kontaktní informace** zadejte kontaktní informace místa.
7. Zvolte **Uložit**.

## <a name="add-a-recruiting-request"></a>Přidání žádosti o nábor

Manažeři mohou odesílat žádosti o nábor v Human Resources. Pokud používáte samostatnou náborovou aplikaci, po dokončení těchto kroků odešlete žádost o nábor a zahájíte proces náboru v této aplikaci. V opačném případě dokončením tohoto postupu zahájíte pracovní postup pro svůj vlastní interní proces náboru.

1. Vyberte **Samoobsluha pro zaměstnance**.
2. Vyberte kartu **Můj tým**.
3. Vyberte **Žádost o nábor**.

    ![Zahájení žádosti o nábor.](./media/hr-recruit-1-request-to-recruit.png)

4. Vyplňte pole **Popis**, **Práce** a **Odhadované počáteční datum**.

    ![Vyplnění žádosti o nábor.](./media/hr-recruit-2-request-to-recruit.png)

5. Vyberte **Pokračovat**. Zobrazí se žádost o nábor pro vaši pozici.
6. V části **Obecné** vyberte náboráře z rozevíracího seznamu **Náborář** a poté vyberte umístění z rozevíracího seznamu **Umístění žádosti na nábor**.
7. V části **Práce** podle potřeby změňte informace a poté vyberte **Vytvořit podrobnosti z práce**.

    ![Vytvořte podrobnosti z úlohy.](./media/hr-recruit-3-create-details-from-job.png)

    Zbytek žádosti o nábor se naplní výchozími informacemi o zadané práci.

8. V části **Vnější popis** zadejte popis práce, který se bude zobrazovat navenek.
9. V části **Pozice** vyberte **Přidat** a poté vyberte pozici pro tuto žádost o nábor.<!--note from editor: In all of these images, are they approved fictitious names, or do they come from sample data included with the app?-->

    ![Přidání pozice.](./media/hr-recruit-4-select-position.png)

10. V části **Dovednosti** vyberte **Přidat** a poté vyberte dovednost.
11. V části **Požadavky na vzdělání** vyberte **Přidat** a poté vyberte hodnoty z rozevíracích nabídek **Vzdělání** a **Úroveň vzdělání**.

    ![Přidání dalších požadavků.](./media/hr-recruit-5-select-educational-requirements.png)

12. V části **Komentář** podle potřeby přidávejte komentáře.
13. V části **Kompenzace** vyberte úroveň z rozevíracího seznamu **Úroveň** a poté upravte **Dolní prahová hodnota**, **Kontrolní bod** a **Horní prahová hodnota**, jak je potřeba.
14. Když je vaše žádost o nábor dokončen a jste připraveni zahájit proces náboru, vyberte **Aktivovat** v řádku nabídek.

    ![Aktivace žádosti o nábor.](./media/hr-recruit-6-activate-recruit-request.png)

15. Zvolte možnost **Uložit**.

## <a name="view-and-edit-your-recruiting-requests"></a>Zobrazení a úpravy žádostí o nábor

Pokud jste manažer a chcete zobrazit své vlastní požadavky:

1. Vyberte **Samoobsluha pro zaměstnance**.
2. Vyberte kartu **Můj tým**.
3. V části **Informace o mém týmu** vyberte kartu **Žádosti o nábor**.

    ![Výběr karty Žádosti o nábor.](./media/hr-recruit-7-recruiting-requests.png)

4. Chcete-li zobrazit nebo upravit žádost o nábor, vyberte jej v mřížce.

Pokud jste personalista a chcete zobrazit všechny žádosti o nábor:

1. Vyberte **Správa zaměstnanců**.
2. Vyberte **Žádosti o nábor**.

    ![Zobrazení žádostí o nábor ve správě zaměstnanců.](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Chcete-li zobrazit nebo upravit žádost o nábor, vyberte jej v mřížce.

## <a name="add-or-edit-a-candidate-profile"></a>Přidání nebo úprava profilu kandidáta

Pokud vaše organizace integrovala jinou aplikaci pro správu žádostí o nábor, žádosti o nábor se předají této aplikaci. Náborová aplikace poté odešle informace o kandidátovi zpět do Human Resources. V opačném případě můžete sledovat vlastní interní procesy náboru a zadávat informace o kandidátech ručně.

1. Vyberte **Správa zaměstnanců**.
2. Vybrerte **Odkazy**.
3. V části **Nábor** vyberte **Kandidáti**.

    ![Zobrazení kandidátů.](./media/hr-recruit-9-candidates.png)

4. Chcete-li přidat kandidáta, vyberte **Nový**. Chcete-li upravit existujícího kandidáta, vyberte jej ze seznamu a pak vyberte možnost **Upravit**. Zobrazí se profil kandidáta.
5. V části **Souhrn kandidáta** podle potřeby zadejte nebo upravte informace o kandidátovi.
6. V části **Žádosti o nábor** vyberte žádost o nábor, se kterou chcete kandidáta propojit. Poté dle potřeby vyplňte pole **Odhadované počáteční datum**, **Náborový manažer**, **Pozice** a **Popis**.

    ![Odkaz na žádost o nábor.](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Vyplňte všechny informace v následujících oblastech, které chcete zahrnout do záznamu kandidáta:

    - **Komentáře**
    - **Profesionální zkušenosti**
    - **Kontaktní informace**
    - **Vzdělání**
    - **Dovednosti**
    - **Certifikáty**
    - **Prověřování**

8. Zvolte **Uložit**.

## <a name="hire-a-candidate"></a>Přijetí kandidáta

Až budete připraveni přijmout kandidáta, postupujte podle tohoto postupu a přeměňte kandidáta na zaměstnance.

1. Na stránce **Kandidát** vyberte **Přijmout**.

    ![Přijetí kandidáta.](./media/hr-recruit-11-hire.png)

2. Na stránce **Přijetí nového pracovníka** pod **Podrobnosti** vyplňte všechna pole.

    ![Zadání podrobností nového zaměstnance.](./media/hr-recruit-12-hire-new-worker.png)

3. Pod **Podrobnosti o pozici** ověřte a podle potřeby změňte informace.
4. V části **Kontrolní seznamy náboru** vyberte příslušné kontrolní seznamy náboru pro tohoto zaměstnance.
5. Volbou **Pokračovat** vytvoříte záznam zaměstnance.

    > [!NOTE]
    > V závislosti na pracovních postupech vaší organizace může záznam kandidáta projít dalšími schvalovacími kroky, než se stane záznamem zaměstnance.

## <a name="decide-not-to-hire-a-candidate"></a>Rozhodnutí o nepřijatí kandidáta

Pokud se rozhodnete kandidáta nepřijmout, postupujte podle tohoto postupu, kterým jej vyřadíte z procesu prověřování. 

1. Na stránce **Kandidát** vyberte **Nepřijmout**.

    ![Nepřijetí kandidáta.](./media/hr-recruit-13-do-not-hire.png)

2. Vyberte **Kód důvodu** a přidejte veškeré potřebné komentáře.
3. Vyberte **OK**.

## <a name="dismiss-a-candidate"></a>Propuštění kandidáta

V případě potřeby můžete kandidáta poté, co ho přijmete, propustit. Například kandidát může vaši nabídku odmítnout nebo se neobjeví hned první den.

- Na stránce **Kandidát** vyberte **Propustit kandidáta**.

    ![Zamítnout kandidáta.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Viz také

[Konfigurace virtuálních tabulek Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Organizování zaměstnanců](hr-personnel-departments-jobs-positions.md)<br>
[Nastavení komponent práce](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
