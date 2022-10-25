---
title: Nakonfigurujte řešení Invoice Capture
description: Tento článek vysvětluje, jak nakonfigurovat řešení Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691132"
---
# <a name="configure-the-invoice-capture-solution"></a>Nakonfigurujte řešení Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Po instalaci řešení Invoice Capture musíte nakonfigurovat prostředí. Proces se skládá z následujících základních kroků.

1. **Požadované:** Synchronizujte právnické osoby z Microsoft Dynamics 365 Finance. Tento krok se používá k nastavení organizační struktury v Microsoft Power Platform.
2. **Požadované:** Nakonfigurujte kanály pro import obrázků faktur. Řešení podporuje následující kanály:

    - Office 365 Outlook (výchozí)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **Volitelný:** Definujte další konfigurační skupiny pro službu optického rozpoznávání znaků (OCR).
4. **Volitelný:** Definujte pravidla mapování pro právnickou osobu, účet dodavatele, položku a typ nákupu.

Tento článek je zaměřen na dva požadované kroky procesu. Další informace o konfiguračních skupinách viz [Skupiny konfigurace řešení Invoice Capture](invoice-capture-config-group.md). Další informace o pravidlech mapování viz [Pravidla mapování řešení Invoice Capture](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Spravovat právnické osoby

Finance definuje právnické osoby jako organizace, které jsou identifikovány prostřednictvím registrace u právního orgánu. Obchodní činnost je vykonávána a evidována v samostatných právnických osobách. V Microsoft Power Platform, obchodní jednotky, role zabezpečení a uživatelé jsou spolu propojeni způsobem, který odpovídá bezpečnostnímu modelu založenému na rolích.

Obchodní jednotky se používají společně s rolemi zabezpečení k řízení přístupu k datům. Uživatelé vidí pouze informace, které potřebují ke své práci. Řešení Invoice Capture poskytuje konfigurační prostor, kde můžete načíst základní informace o existujících právnických osobách ve Finance a spravovat ty subjekty, které jsou vytvořeny ručně. Právnické osoby se používají na fakturách dodavatelů a při bezpečnostní kontrole.

Když je vytvořena právnická osoba a zobrazena v zobrazení seznamu, automaticky se vytvoří výchozí obchodní jednotka se stejným názvem. Týmu je udělena bezpečnostní role **pracovník AP**. Při importu právnických osob se importují základní kmenová data z Finance. Neexistující položky budou identifikovány právnickou osobou a budou přidány do řešení Invoice Capture. Výchozí konfigurační skupina je přiřazena novým právnickým osobám.

### <a name="sync-legal-entities"></a>Synchronizovat právnické osoby

Nelze vytvořit právnické osoby přímo. Z Finance však můžete synchronizovat právnické osoby. Chcete-li synchronizovat právnické osoby, postupujte takto.

1. Přejděte na **Nastavení \> Nastavení systému \> Správa právnických osob**.
2. Vyberte **Synchronizovat právnické osoby** a pak vyberte **OK** v potvrzovacím dialogovém okně.

Po dokončení synchronizace se zobrazí počet nových právnických osob. Nové právnické osoby se zobrazí v zobrazení seznamu. Výchozí konfigurační skupina je přiřazena novým právnickým osobám.

## <a name="configure-invoice-import-channels"></a>Konfigurace kanálů pro import faktur

Dodavatelé odesílají faktury z různých kanálů (e-mail, pracovní prostor souborů nebo fakturační portál) prostřednictvím různých formátů (papír nebo obrázek). Řešení pro zachycení faktur zvládne různé kanály a formáty. Podporovány jsou následující typy:

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

Když je vytvořen kanál pro konkrétní účet, je vytvořen automatizovaný tok, který má předdefinovanou šablonu, aby monitoroval příchozí e-maily nebo soubory v doručené poště nebo v prostoru. Jakýkoli soubor, který má platnou fakturu, může být rozpoznán a odeslán do oblasti faktur, kde bude čekat na zpracování pracovníkem pro závazky (AP). Příloha by měla být ve formátu PDF nebo obrázku. Faktury lze načíst do řešení pro zachycení faktur podle konfigurace kanálu.

### <a name="create-a-channel"></a>Vytvoření kanálu

Pokud jste importovali další balíček řešení (Dynamics 365 Invoice Capture – Installation Tools), výchozí připojení pro Office 365 Outlook je připraveno k použití. Pokud chcete vytvořit více připojení pro různé e-mailové účty nebo jiné typy kanálů, viz [Vytvořte další připojení pro kanály](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Při vytváření kanálu postupujte takto.

1. Přejděte na **Nastavení \> Nastavení systému \> Konfigurace kanálů**.
2. Zvolte **Nové**.
3. Nastavte následující pole:

    - Název kanálu
    - Popis
    - Typ
    - Připojení

Do řešení lze importovat pouze e-maily nebo soubory, které splňují následující kritéria.

| Typ               | Konfigurace  | Další informace |
|--------------------|----------------|------------------|
| Office 365 Outlook | Složka         | E-mailová složka musí být v kořenovém adresáři. Ve výchozím nastavení je použita složka příchozí pošty. Podsložky nejsou podporovány. |
|                    | Filtr předmětu | (Volitelné) Podřetězec, který by měl být součástí předmětu. |
|                    | Z           | (Volitelné) E-mailová adresa odesílatele nebo odesílatelů. Chcete-li zadat více adres, použijte jako oddělovače středník (;). |
| SharePoint         | Adresa webu   | Adresa URL webu. |
|                    | Složka         | Složka v adrese webu. |

### <a name="activate-the-channel"></a>Aktivace kanálu

Když je tok uložen, pole zobrazují stav kanálu a čas, kdy byl vytvořen. V původním stavu je pole **Stav** nastaveno na **Neaktivní**. Pole **Důvod stavu** indikuje, že kanál byl inicializován a je připraven k aktivaci.

Chcete-li kanál aktivovat, zaškrtněte políčko **Aktivovat**. Pole **Stav** a **Důvod stavu** jsou aktualizována.

Pokud kanál nepotřebujete, můžete jej deaktivovat. Chcete-li kanál deaktivovat, vyberte **Deaktivovat**. Pole **Stav** a **Důvod stavu** jsou aktualizována.

### <a name="manage-flows-in-flow-management"></a>Spravujte toky ve správě toků

Kanál můžete sledovat na stránce **Konfigurace kanálů** nebo ve správě toku.

Chcete-li zobrazit další podrobnosti, přejděte na **Systém správce \> Výchozí řešení \> Cloudové toky** a vyberte cílový tok. Zobrazené podrobnosti zahrnují propojená připojení, vlastníky a historii běhů.

Chcete-li synchronizovat stav, vyberte **Kontrola** pro potvrzení, že stav kanálu odpovídá stavu toku.

Některé případy zpracování výjimek jsou uvedeny v poli **Důvod stavu**:

- **Chybějící připojení Dataverse** – Aktuální uživatel nevytvořil alespoň jedny informace o připojení **Microsoft Dataverse**.
- **Nenalezeno** – Tok, který je propojen s kanálem, byl ve správě toku odstraněn. Pro vytvoření nového kanálu by měl být kanál znovu uložen.
- **Deaktivováno ve správě toku** – Tok byl deaktivován ve správě toku a stav kanálu se liší od stavu toku.
- **Aktivováno ve správě toku** – Tok byl aktivován ve správě toku a stav kanálu se liší od stavu toku.
- **Vyskytla se neočekávaná chyba** – Uživatel musí potvrdit, že web je „Komunikační web“ a že složka je „Knihovna dokumentů“.
