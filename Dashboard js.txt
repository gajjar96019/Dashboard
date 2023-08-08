import { Container, Button, Navbar, Offcanvas, Nav, NavDropdown, Form } from 'react-bootstrap';
import { AiOutlineSearch, AiFillAppstore, AiFillPieChart } from "react-icons/ai";
import { IoIosNotificationsOutline } from "react-icons/io";
import { PiChatsCircle } from "react-icons/pi";
import { BiBarChart } from "react-icons/bi";
import { FaUserPlus } from "react-icons/fa";
import { LiaExpandArrowsAltSolid, LiaShoppingBagSolid } from "react-icons/lia";

function Dashboard() {
    return (
        <>
            {[false].map((expand) => (
                <Navbar key={expand} expand={expand} className="bg-body-tertiary mb-3">
                    <Container fluid>
                        <div className='d-flex justify-content-between'>
                            <Navbar.Toggle aria-controls={`offcanvasNavbar-expand-${expand}`} />
                            <Navbar.Offcanvas
                                id={`offcanvasNavbar-expand-${expand}`}
                                aria-labelledby={`offcanvasNavbarLabel-expand-${expand}`}
                                placement="start"
                            >
                                <Offcanvas.Header closeButton>
                                    <Offcanvas.Title id={`offcanvasNavbarLabel-expand-${expand}`}>
                                        Offcanvas
                                    </Offcanvas.Title>
                                </Offcanvas.Header>
                                <Offcanvas.Body>
                                    <Nav className="justify-content-end flex-grow-1 pe-3">
                                        <Nav.Link href="#action1">Home</Nav.Link>
                                        <Nav.Link href="#action2">Link</Nav.Link>
                                        <NavDropdown
                                            title="Dropdown"
                                            id={`offcanvasNavbarDropdown-expand-${expand}`}
                                        >
                                            <NavDropdown.Item href="#action3">Action</NavDropdown.Item>
                                            <NavDropdown.Item href="#action4">
                                                Another action
                                            </NavDropdown.Item>
                                            <NavDropdown.Divider />
                                            <NavDropdown.Item href="#action5">
                                                Something else here
                                            </NavDropdown.Item>
                                        </NavDropdown>
                                    </Nav>
                                    <Form className="d-flex">
                                        <Form.Control
                                            type="search"
                                            placeholder="Search"
                                            className="me-2"
                                            aria-label="Search"
                                        />
                                        <Button variant="outline-success">Search</Button>
                                    </Form>
                                </Offcanvas.Body>
                            </Navbar.Offcanvas>
                            <div className='d-flex justify-content-between'>
                                <div className='d-flex ms-5'>
                                    <Navbar href="#">Home</Navbar>
                                    <Navbar href="#" className='ms-5'>Contact</Navbar>
                                </div>
                            </div>
                        </div>
                        <div className='icon text-secondary d-flex'>
                            <h1><AiOutlineSearch size={20} /></h1>
                            <h1><PiChatsCircle size={20} /></h1>
                            <h1><IoIosNotificationsOutline size={20} /></h1>
                            <h1><LiaExpandArrowsAltSolid size={20} /></h1>
                            <h1><AiFillAppstore size={20} /></h1>
                        </div>
                    </Container>
                </Navbar>
            ))}

            <div className='inner'>
                <Container fluid>
                    <div className='text-start'>
                        <div className='d-flex justify-content-between align-items-center pb-3'>
                            <div>
                                <h4>Dashboard</h4>
                            </div>
                            <div>
                                <span className='text-primary'>Home </span>
                                <span>/ Dashboard v1</span>
                            </div>
                        </div>

                        <div className='cards'>

                            <div className='Boxes'>
                                <div className="row">

                                    <div className="col-3">
                                        <div className='box-1 rounded ps-2 pt-3 text-white'>
                                            <h2 className='fw-bold'>150</h2>
                                            <div className='logo'>
                                                <h1 className='display-1'><LiaShoppingBagSolid /></h1>
                                            </div>
                                            <span>New Orders</span>
                                            <div className='info text-center'>
                                                <span>More Info</span>
                                            </div>
                                        </div>
                                    </div>

                                    <div className="col-3">
                                        <div className='box-1 box-2 rounded ps-2 pt-3 text-white'>
                                            <h2 className='fw-bold'>53%</h2>
                                            <div className='logo'>
                                                <h1 className='display-1'><BiBarChart /></h1>
                                            </div>
                                            <span>Bounce Rate</span>
                                            <div className='info info-2 text-center'>
                                                <span>More Info</span>
                                            </div>
                                        </div>
                                    </div>

                                    <div className="col-3">
                                        <div className='box-1 box-3 rounded ps-2 pt-3'>
                                            <h2 className='fw-bold'>44</h2>
                                            <div className='logo'>
                                                <h1 className='display-1'><FaUserPlus /></h1>
                                            </div>
                                            <span>User Registrations</span>
                                            <div className='info info-3 text-center'>
                                                <span>More Info</span>
                                            </div>
                                        </div>
                                    </div>

                                    <div className="col-3">
                                        <div className='box-1 bg-danger rounded ps-2 pt-3 text-white'>
                                            <h2 className='fw-bold'>65</h2>
                                            <div className='logo logo-4'>
                                                <h1 className='display-1'><AiFillPieChart /></h1>
                                            </div>
                                            <span>Unique Visitors</span>
                                            <div className='info info-4 text-center'>
                                                <span>More Info</span>
                                            </div>
                                        </div>
                                    </div>

                                </div>
                            </div>

                        </div>
                    </div>
                </Container>
            </div>
        </>
    )
}

export default Dashboard;
