# System Design

## Use Case Diagram

<svg width="100%" viewBox="0 0 1700 1320" xmlns="http://www.w3.org/2000/svg" role="img">
<title>Use case diagram for Gym Membership and Class Scheduling System</title>
<desc>UML use case diagram showing Member, Trainer, Front Desk Staff, Admin/Manager and Payment Gateway actors interacting with system use cases, with include, extend and generalization relationships.</desc>
<rect x="0" y="0" width="1700" height="1320" fill="#FFFFFF"/>
<defs>
<marker id="openArrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="8" markerHeight="8" orient="auto-start-reverse">
<path d="M1 1 L9 5 L1 9" fill="none" stroke="context-stroke" stroke-width="1.5"/>
</marker>
<marker id="hollowTriangle" viewBox="0 0 12 12" refX="11" refY="6" markerWidth="12" markerHeight="12" orient="auto-start-reverse">
<path d="M1 1 L11 6 L1 11 Z" fill="white" stroke="context-stroke" stroke-width="1"/>
</marker>
</defs>
<rect x="180" y="80" width="1360" height="820" rx="6" fill="#FAFAF8" stroke="#444441" stroke-width="1.5"/>
<text x="860.0" y="108" text-anchor="middle" font-family="Arial, sans-serif" font-size="17" font-weight="bold" fill="#2C2C2A">Gym Membership &amp; Class Scheduling System</text>
<ellipse cx="350" cy="190" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="350" y="190" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Register Account</text>
<ellipse cx="700" cy="190" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="700" y="190" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Login</text>
<ellipse cx="1050" cy="190" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="1050" y="190" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Manage Profile</text>
<ellipse cx="1400" cy="190" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="1400" y="190" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Browse Class Schedule</text>
<ellipse cx="350" cy="340" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="350" y="340" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Book Class</text>
<ellipse cx="700" cy="340" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="700" y="331" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Check Class</text>
<text x="700" y="349" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Availability</text>
<ellipse cx="1050" cy="340" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="1050" y="340" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Cancel Booking</text>
<ellipse cx="1400" cy="340" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="1400" y="340" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Purchase Membership</text>
<ellipse cx="350" cy="490" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="350" y="490" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Renew Membership</text>
<ellipse cx="700" cy="490" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="700" y="481" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Upgrade Membership</text>
<text x="700" y="499" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Plan</text>
<ellipse cx="1050" cy="490" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="1050" y="490" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Make Payment</text>
<ellipse cx="1400" cy="490" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="1400" y="481" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Manage Class</text>
<text x="1400" y="499" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Schedule</text>
<ellipse cx="350" cy="640" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="350" y="631" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Pay via Online</text>
<text x="350" y="649" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Gateway</text>
<ellipse cx="700" cy="640" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="700" y="631" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Pay via Cash /</text>
<text x="700" y="649" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Manual</text>
<ellipse cx="1050" cy="640" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="1050" y="640" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Check-in to Gym</text>
<ellipse cx="1400" cy="640" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="1400" y="631" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Process Partial</text>
<text x="1400" y="649" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Refund</text>
<ellipse cx="350" cy="790" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="350" y="781" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Assign Trainer</text>
<text x="350" y="799" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">to Class</text>
<ellipse cx="700" cy="790" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="700" y="781" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Mark Class</text>
<text x="700" y="799" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Attendance</text>
<ellipse cx="1050" cy="790" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="1050" y="781" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Manage Members</text>
<text x="1050" y="799" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">&amp; Trainers</text>
<ellipse cx="1400" cy="790" rx="105" ry="42" fill="#E6F1FB" stroke="#185FA5" stroke-width="1.5"/>
<text x="1400" y="790" text-anchor="middle" dominant-baseline="central" font-family="Arial, sans-serif" font-size="14" fill="#0C447C">Generate Reports</text>
<circle cx="90" cy="292" r="14" fill="none" stroke="#2C2C2A" stroke-width="2"/>
<line x1="90" y1="306" x2="90" y2="355" stroke="#2C2C2A" stroke-width="2"/>
<line x1="68" y1="322" x2="112" y2="322" stroke="#2C2C2A" stroke-width="2"/>
<line x1="90" y1="355" x2="70" y2="390" stroke="#2C2C2A" stroke-width="2"/>
<line x1="90" y1="355" x2="110" y2="390" stroke="#2C2C2A" stroke-width="2"/>
<text x="90" y="410" text-anchor="middle" font-family="Arial, sans-serif" font-size="13" font-weight="bold" fill="#2C2C2A">Member</text>
<circle cx="90" cy="712" r="14" fill="none" stroke="#2C2C2A" stroke-width="2"/>
<line x1="90" y1="726" x2="90" y2="775" stroke="#2C2C2A" stroke-width="2"/>
<line x1="68" y1="742" x2="112" y2="742" stroke="#2C2C2A" stroke-width="2"/>
<line x1="90" y1="775" x2="70" y2="810" stroke="#2C2C2A" stroke-width="2"/>
<line x1="90" y1="775" x2="110" y2="810" stroke="#2C2C2A" stroke-width="2"/>
<text x="90" y="830" text-anchor="middle" font-family="Arial, sans-serif" font-size="13" font-weight="bold" fill="#2C2C2A">Trainer /</text>
<text x="90" y="846" text-anchor="middle" font-family="Arial, sans-serif" font-size="13" font-weight="bold" fill="#2C2C2A">Instructor</text>
<circle cx="1610" cy="292" r="14" fill="none" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1610" y1="306" x2="1610" y2="355" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1588" y1="322" x2="1632" y2="322" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1610" y1="355" x2="1590" y2="390" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1610" y1="355" x2="1630" y2="390" stroke="#2C2C2A" stroke-width="2"/>
<text x="1610" y="410" text-anchor="middle" font-family="Arial, sans-serif" font-size="13" font-weight="bold" fill="#2C2C2A">Front Desk</text>
<text x="1610" y="426" text-anchor="middle" font-family="Arial, sans-serif" font-size="13" font-weight="bold" fill="#2C2C2A">Staff</text>
<circle cx="1610" cy="712" r="14" fill="none" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1610" y1="726" x2="1610" y2="775" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1588" y1="742" x2="1632" y2="742" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1610" y1="775" x2="1590" y2="810" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1610" y1="775" x2="1630" y2="810" stroke="#2C2C2A" stroke-width="2"/>
<text x="1610" y="830" text-anchor="middle" font-family="Arial, sans-serif" font-size="13" font-weight="bold" fill="#2C2C2A">Admin /</text>
<text x="1610" y="846" text-anchor="middle" font-family="Arial, sans-serif" font-size="13" font-weight="bold" fill="#2C2C2A">Manager</text>
<circle cx="1050" cy="1072" r="14" fill="none" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1050" y1="1086" x2="1050" y2="1135" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1028" y1="1102" x2="1072" y2="1102" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1050" y1="1135" x2="1030" y2="1170" stroke="#2C2C2A" stroke-width="2"/>
<line x1="1050" y1="1135" x2="1070" y2="1170" stroke="#2C2C2A" stroke-width="2"/>
<text x="1050" y="1190" text-anchor="middle" font-family="Arial, sans-serif" font-size="13" font-weight="bold" fill="#2C2C2A">Payment Gateway</text>
<text x="1050" y="1206" text-anchor="middle" font-family="Arial, sans-serif" font-size="13" font-weight="bold" fill="#2C2C2A">(external)</text>
<path d="M 90.0 340.0 L 189.8 319.8 L 189.8 244.8 L 189.8 244.8 L 189.8 190.0 L 245.0 190.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="245.0" cy="190.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 340.0 L 194.2 324.2 L 194.2 249.2 L 509.2 249.2 L 509.2 190.0 L 595.0 190.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="595.0" cy="190.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 340.0 L 198.8 328.8 L 198.8 253.8 L 863.8 253.8 L 863.8 190.0 L 945.0 190.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="945.0" cy="190.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 340.0 L 203.2 333.2 L 203.2 258.2 L 1218.2 258.2 L 1218.2 190.0 L 1295.0 190.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="1295.0" cy="190.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 340.0 L 207.8 337.8 L 207.8 412.8 L 207.8 412.8 L 207.8 340.0 L 245.0 340.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="245.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 340.0 L 212.2 342.2 L 212.2 417.2 L 877.2 417.2 L 877.2 340.0 L 945.0 340.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="945.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 340.0 L 216.8 346.8 L 216.8 421.8 L 1231.8 421.8 L 1231.8 340.0 L 1295.0 340.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="1295.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 340.0 L 221.2 351.2 L 221.2 426.2 L 221.2 426.2 L 221.2 490.0 L 245.0 490.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="245.0" cy="490.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 340.0 L 225.8 355.8 L 225.8 430.8 L 540.8 430.8 L 540.8 490.0 L 595.0 490.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="595.0" cy="490.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 340.0 L 230.2 360.2 L 230.2 585.2 L 895.2 585.2 L 895.2 640.0 L 945.0 640.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="945.0" cy="640.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 760.0 L 203.2 753.2 L 203.2 258.2 L 518.2 258.2 L 518.2 190.0 L 595.0 190.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="760.0" r="2.4" fill="#5F5E5A"/>
<circle cx="595.0" cy="190.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 760.0 L 207.8 757.8 L 207.8 262.8 L 872.8 262.8 L 872.8 190.0 L 945.0 190.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="760.0" r="2.4" fill="#5F5E5A"/>
<circle cx="945.0" cy="190.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 760.0 L 212.2 762.2 L 212.2 567.2 L 1227.2 567.2 L 1227.2 490.0 L 1295.0 490.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="760.0" r="2.4" fill="#5F5E5A"/>
<circle cx="1295.0" cy="490.0" r="2.4" fill="#5F5E5A"/>
<path d="M 90.0 760.0 L 216.8 766.8 L 216.8 721.8 L 531.8 721.8 L 531.8 790.0 L 595.0 790.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="90.0" cy="760.0" r="2.4" fill="#5F5E5A"/>
<circle cx="595.0" cy="790.0" r="2.4" fill="#5F5E5A"/>
<path d="M 1610.0 340.0 L 1513.2 333.2 L 1513.2 258.2 L 868.2 258.2 L 868.2 190.0 L 805.0 190.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="1610.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="805.0" cy="190.0" r="2.4" fill="#5F5E5A"/>
<path d="M 1610.0 340.0 L 1517.8 337.8 L 1517.8 562.8 L 1222.8 562.8 L 1222.8 640.0 L 1155.0 640.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="1610.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="1155.0" cy="640.0" r="2.4" fill="#5F5E5A"/>
<path d="M 1610.0 340.0 L 1522.2 342.2 L 1522.2 717.2 L 1227.2 717.2 L 1227.2 790.0 L 1155.0 790.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="1610.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="1155.0" cy="790.0" r="2.4" fill="#5F5E5A"/>
<path d="M 1610.0 340.0 L 1526.8 346.8 L 1526.8 571.8 L 881.8 571.8 L 881.8 640.0 L 805.0 640.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="1610.0" cy="340.0" r="2.4" fill="#5F5E5A"/>
<circle cx="805.0" cy="640.0" r="2.4" fill="#5F5E5A"/>
<path d="M 1610.0 760.0 L 1511.0 751.0 L 1511.0 256.0 L 866.0 256.0 L 866.0 190.0 L 805.0 190.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="1610.0" cy="760.0" r="2.4" fill="#5F5E5A"/>
<circle cx="805.0" cy="190.0" r="2.4" fill="#5F5E5A"/>
<path d="M 1610.0 760.0 L 1515.5 755.5 L 1515.5 560.5 L 1515.5 560.5 L 1515.5 490.0 L 1505.0 490.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="1610.0" cy="760.0" r="2.4" fill="#5F5E5A"/>
<circle cx="1505.0" cy="490.0" r="2.4" fill="#5F5E5A"/>
<path d="M 1610.0 760.0 L 1520.0 760.0 L 1520.0 715.0 L 525.0 715.0 L 525.0 790.0 L 455.0 790.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="1610.0" cy="760.0" r="2.4" fill="#5F5E5A"/>
<circle cx="455.0" cy="790.0" r="2.4" fill="#5F5E5A"/>
<path d="M 1610.0 760.0 L 1524.5 764.5 L 1524.5 719.5 L 1229.5 719.5 L 1229.5 790.0 L 1155.0 790.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="1610.0" cy="760.0" r="2.4" fill="#5F5E5A"/>
<circle cx="1155.0" cy="790.0" r="2.4" fill="#5F5E5A"/>
<path d="M 1610.0 760.0 L 1529.0 769.0 L 1529.0 724.0 L 1529.0 724.0 L 1529.0 790.0 L 1505.0 790.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="1610.0" cy="760.0" r="2.4" fill="#5F5E5A"/>
<circle cx="1505.0" cy="790.0" r="2.4" fill="#5F5E5A"/>
<path d="M 1050.0 1120.0 L 1050.0 865.0 L 210.0 865.0 L 210.0 640.0 L 245.0 640.0" fill="none" stroke="#5F5E5A" stroke-width="1.1"/>
<circle cx="1050.0" cy="1120.0" r="2.4" fill="#5F5E5A"/>
<circle cx="245.0" cy="640.0" r="2.4" fill="#5F5E5A"/>
<line x1="455.0" y1="340.0" x2="595.0" y2="340.0" stroke="#993C1D" stroke-width="1.3" stroke-dasharray="6,4" marker-end="url(#openArrow)"/><rect x="483.0" y="318.0" width="84" height="16" fill="#FAFAF8"/><text x="525.0" y="326.0" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" font-style="italic" fill="#993C1D">&lt;&lt;include&gt;&gt;</text>
<line x1="1303.5" y1="356.5" x2="1146.5" y2="473.5" stroke="#993C1D" stroke-width="1.3" stroke-dasharray="6,4" marker-end="url(#openArrow)"/><rect x="1183.0" y="393.0" width="84" height="16" fill="#FAFAF8"/><text x="1225.0" y="401.0" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" font-style="italic" fill="#993C1D">&lt;&lt;include&gt;&gt;</text>
<path d="M 445.1 507.8 L 445.1 565.0 L 954.9 565.0 L 954.9 507.8" fill="none" stroke="#993C1D" stroke-width="1.3" stroke-dasharray="6,4" marker-end="url(#openArrow)"/>
<rect x="310.0" y="557.0" width="90" height="16" fill="#FAFAF8"/>
<text x="355.0" y="565.0" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" font-style="italic" fill="#993C1D">&lt;&lt;include&gt;&gt;</text>
<line x1="805.0" y1="490.0" x2="945.0" y2="490.0" stroke="#993C1D" stroke-width="1.3" stroke-dasharray="6,4" marker-end="url(#openArrow)"/><rect x="833.0" y="468.0" width="84" height="16" fill="#FAFAF8"/><text x="875.0" y="476.0" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" font-style="italic" fill="#993C1D">&lt;&lt;include&gt;&gt;</text>
<line x1="1320.3" y1="612.7" x2="1129.7" y2="367.3" stroke="#993C1D" stroke-width="1.3" stroke-dasharray="6,4" marker-end="url(#openArrow)"/><rect x="1183.0" y="468.0" width="84" height="16" fill="#FAFAF8"/><text x="1225.0" y="476.0" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" font-style="italic" fill="#993C1D">&lt;&lt;extend&gt;&gt;</text>
<line x1="452.7" y1="631.2" x2="947.3" y2="498.8" stroke="#0F6E56" stroke-width="1.3" marker-end="url(#hollowTriangle)"/>
<line x1="796.5" y1="623.5" x2="953.5" y2="506.5" stroke="#0F6E56" stroke-width="1.3" marker-end="url(#hollowTriangle)"/>
<path d="M 1610 702 C 1490 592, 1490 510, 1610 400" fill="none" stroke="#0F6E56" stroke-width="1.3" marker-end="url(#hollowTriangle)"/>
<rect x="200" y="910" width="620" height="220" fill="#FFFFFF" stroke="#B4B2A9" stroke-width="1"/>
<text x="220" y="932" font-family="Arial, sans-serif" font-size="15" font-weight="bold" fill="#2C2C2A">Legend</text>
<line x1="220" y1="965" x2="280" y2="965" stroke="#5F5E5A" stroke-width="1.5"/>
<text x="295" y="970" font-family="Arial, sans-serif" font-size="13" fill="#2C2C2A">Association (actor participates in use case)</text>
<line x1="220" y1="997" x2="280" y2="997" stroke="#993C1D" stroke-width="1.5" stroke-dasharray="6,4" marker-end="url(#openArrow)"/>
<text x="295" y="1002" font-family="Arial, sans-serif" font-size="13" fill="#2C2C2A">&lt;&lt;include&gt;&gt; / &lt;&lt;extend&gt;&gt; dependency</text>
<line x1="220" y1="1029" x2="280" y2="1029" stroke="#0F6E56" stroke-width="1.5" marker-end="url(#hollowTriangle)"/>
<text x="295" y="1034" font-family="Arial, sans-serif" font-size="13" fill="#2C2C2A">Generalization (hollow triangle = "is a")</text>
<rect x="220" y="1066" width="26" height="18" fill="#E6F1FB" stroke="#185FA5" stroke-width="1"/>
<text x="255" y="1079" font-family="Arial, sans-serif" font-size="13" fill="#2C2C2A">Use case (oval)</text>
<circle cx="550" cy="1069" r="7" fill="none" stroke="#2C2C2A" stroke-width="1.5"/>
<line x1="550" y1="1076" x2="550" y2="1086" stroke="#2C2C2A" stroke-width="1.5"/>
<text x="565" y="1081" font-family="Arial, sans-serif" font-size="13" fill="#2C2C2A">Actor</text>
</svg>

### Use Case Diagram Description

The system has five main actors:

1. **Members** - End users who use gym facilities
2. **Trainers/Instructors** - Staff conducting classes
3. **Front Desk Staff** - Administrative staff managing operations
4. **Admin/Manager** - System administrators and managers
5. **Payment Gateway** - External payment processing system

#### Member Use Cases
- Register Account
- Login
- Manage Profile
- Browse Class Schedule
- Book Class
- Check Class Availability
- Cancel Booking
- Purchase Membership
- Upgrade Membership
- Renew Membership
- Make Payment
- Check-in to Gym
- Process Refund
- View Membership History

#### Trainer/Instructor Use Cases
- Login
- Assign Trainer to Class
- Mark Class Attendance
- Manage Class Schedule

#### Front Desk Staff Use Cases
- Login
- Manage Class Schedule
- Manage Members & Trainers
- Process Refund
- Pay via Cash/Manual

#### Admin/Manager Use Cases
- Login
- Manage Members
- Manage Trainers
- Manage Classes
- Generate Reports

#### External Actor
- **Payment Gateway** - Processes online payments securely

---

## UI/UX Wireframe

Below is the complete UI/UX wireframe for the Gym Membership & Class Scheduling System showing all user interfaces and flows.

### 1. Login Screen
**Common entry screen for all users (Members, Trainers, Front Desk, Admin)**

- Logo: GYM SYSTEM
- Email/Username input field
- Password input field
- Sign In button
- Link to create new account

---

### 2. Member Dashboard
**Main screen after a Member logs in**

**Left Sidebar Navigation:**
- Dashboard (Active)
- Browse Class Schedule
- My Bookings
- Membership
- Make Payment
- Check-in to Gym
- Manage Profile

**Main Content:**
- Welcome greeting with membership status badge (ACTIVE)
- Stats Cards:
  - Membership Status: Active
  - Upcoming Classes: 3
  - My Bookings: 2
  - Membership Plan: Monthly
- Upcoming Classes Table:
  - Class name, Trainer, Date, Time, Availability (e.g., 11/15 spots)
  - Action buttons for each class

---

### 3. Browse Class Schedule / Book Class
**Member checks availability before booking**

**Screen Layout:**
- Page title: "Browse Class Schedule"
- Filter button for search/filtering
- Table with columns:
  - Class Name
  - Trainer Name
  - Date
  - Time
  - Available Spots (e.g., 11/15)
  - Action Buttons: "Check Availability" | "Book"

**Flow:** Member views class → Checks if spots available → Books class

---

### 4. My Bookings
**Member views confirmed bookings and can cancel**

**Screen Layout:**
- Page title: "My Bookings"
- Table with columns:
  - Class Name
  - Date
  - Booking Status (Confirmed/Cancelled/Attended)
  - Action Button: "Cancel Booking"

---

### 5. Membership & Payment
**Purchase, renew, or upgrade membership, then make payment**

**Section 1: Membership Options (3 Cards)**
1. **Purchase Membership** - Select a membership plan - "Purchase" button
2. **Renew Membership** - Continue current plan - "Renew" button (green)
3. **Upgrade Plan** - Change to better plan - "Upgrade" button

**Section 2: Make Payment (2 Cards)**
1. **Pay via Online Gateway** - External payment system - "Pay Online" button
2. **Pay via Cash/Manual** - Front desk records it - "Pay Cash/Manual" button (green)

---

### 6. Manage Profile
**Member updates personal information**

**Form Fields:**
- Full Name (text input)
- Email (text input)
- Contact/Phone (text input)
- Save Changes button

---

### 7. Check-in to Gym
**Member logs entry to gym**

- Info: "Only active members can check in"
- "CHECK IN NOW" button (primary)
- Check-in History Table:
  - Date column
  - Status column (Checked-in)

---

### 8. Front Desk Staff Dashboard
**Manage schedules, members/trainers, and process refunds**

**Left Sidebar Navigation:**
- Manage Class Schedule (Active)
- Manage Members & Trainers
- Process Refund

**Main Content - Manage Class Schedule:**

**Add Class Section:**
- Input fields:
  - Class Name
  - Trainer Name
  - Date
  - Time
  - Room/Location
- "Add Class" button

**Current Schedule Table:**
- Class Name
- Trainer Name
- Date
- Capacity (Total)
- Booked (Current bookings)
- Action buttons

---

### 9. Trainer/Instructor Dashboard
**Assign trainers and mark class attendance**

**Left Sidebar Navigation:**
- Assign Trainer to Class (Active)
- Mark Class Attendance

**Section 1: Assign Trainer to Class**
- Table columns:
  - Class Name
  - Current Trainer
  - Date
  - Action: "Assign Trainer" button

**Section 2: Mark Class Attendance**
- Table columns:
  - Class Name
  - Members Booked
  - Action: "Mark Attendance" button (green)

---

### 10. Admin/Manager Dashboard
**View system analytics and generate reports**

**Left Sidebar Navigation:**
- Generate Reports (Active)
- Use Cases / Procedures

**Main Content:**

**Analytics Stats (4 Cards):**
- Total Members: 120
- Active Members: 105
- Total Bookings: 78
- Net Payments: ₱85,000

**Reports Section:**
- "Generate Report" button
- "Print Report" button
- Available report types:
  - Member Reports
  - Financial Reports
  - Class Attendance Reports
  - Trainer Performance Reports

---

## UX Flow Diagram

### Flow 1: Member Registration & Login
```
Login/Register → Authenticate → Role Dashboard (Member) → Main Features
```

### Flow 2: Browse & Book Classes
```
Browse Schedule → Check Availability → Book Class → Confirmation
```

### Flow 3: Membership Management
```
Purchase/Renew/Upgrade Membership → Make Payment → Payment Confirmation
```

### Flow 4: Booking Management
```
View My Bookings → Cancel Booking → Process Refund
```

### Flow 5: Class Management (Trainer)
```
Assign Trainer to Class → Mark Attendance → Generate Attendance Report
```

### Flow 6: System Administration
```
Admin Dashboard → View Analytics → Generate Reports → Export/Print
```

---

## Color Scheme

- **Primary (Dark):** #172033 (Dark Blue-Gray)
- **Primary (Light):** #2563eb (Bright Blue)
- **Success:** #bbf7d0 (Light Green)
- **Danger:** #fecaca (Light Red)
- **Background:** #f8fafc (Light Gray)
- **Text:** #172033 (Dark)
- **Secondary Text:** #64748b (Gray)

---

## Key Design Principles

1. **Role-Based Navigation** - Each user role has different sidebar options
2. **Clear Call-to-Action** - Buttons are clearly labeled with actions
3. **Table-Based Data** - Lists shown in organized tables with action buttons
4. **Status Badges** - Visual indicators for membership and booking status
5. **Responsive Layout** - Two-column layout (sidebar + main content)
6. **Consistent Styling** - Uniform button styles, colors, and spacing

---

## Navigation Structure

```
├── Login Page
├── Member Dashboard
│   ├── Browse Class Schedule (Book Class)
│   ├── My Bookings (Cancel Booking)
│   ├── Membership (Purchase/Renew/Upgrade)
│   ├── Make Payment (Online/Cash)
│   ├── Check-in to Gym
│   └── Manage Profile
├── Front Desk Dashboard
│   ├── Manage Class Schedule
│   ├── Manage Members & Trainers
│   └── Process Refund
├── Trainer Dashboard
│   ├── Assign Trainer to Class
│   └── Mark Class Attendance
└── Admin/Manager Dashboard
    └── Generate Reports
```

---

## For Detailed Documentation

- [Database Schema](DATABASE.md) - See table structure and relationships
- [API Documentation](API.md) - See all endpoints and their usage
- [Setup Instructions](SETUP.md) - How to install and run the system
- [Project Structure](PROJECT_STRUCTURE.md) - Code organization guide
